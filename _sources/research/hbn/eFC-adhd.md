---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# edge-centric Functional Connectivity in ADHD subtypes

## Project Description

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private on SIG](https://github.com/sensein/hbn_adhd)|
| **Contributors**| Yibei Chen, Maedbh King, Satra Ghosh* |
| **MIT Project**  | Yes |
| **SIG Project**  | Yes |


## Project Updates

### 12/04/2023 - 12/08/2023
- unexpected updates: Jeff checked my code for selecting neurotypical subjects and found that I have mistakenly relaxed the criteria, which means that my NT group probably has subjects that are not NT enough. Here is the message from Jeff:
  ```
  you are including “No Diagnosis Given: Incomplete Eval” and i exclude them
  the threshold seems to be a count of how many diagnoses someone has. so as it is lowered, that means it will allow people with increasing numbers of diagnoses, for example, it will include someone if they have just 1 diagnosis of ADHD or whatever
  ```
- I will come back to this late Janurary to see whether correctly NT group will make our null results different

**12/01/2023: Pause**

### 10/23/2023 - 10/27/2023
- there are two stages for this method, the first one is to get (n_parcel, n_parcel, n_TR) matrix, there are still ~400-subject-calculation (movie DM) ongoing due to preempted jobs & my misestimated saving strategy
- at the second stage, there are two branches to go:
  - RMS (n, n_TR), the 17-network one (17, n_TR) I did before thru averaging discounts edge characteristics, but I manually checked one participant's results and mapped TRs back to stimuli time, those spikes perfectly matches scene changes, especially spikes from the attention network. Now I decide to move to global RMS (1, n_TR), then go from here
    - try classification at this stage (SVM, RBF) for three types with engineered features
    - we should also combine those spikes with eFC
  - edge-centric FC (n_edge, n_edge), this is the functional connectivity matrix, should be the core part of this paper but I need to think more about how to use it
- other notes from meeting w/ SG & MK (mostly after OHBM)
  - subcortical, cerebellum (cifti)
  - behavioral data
  - eFC vs DICE?

### 10/16/2023 - 10/20/2023
- Last time I decided to compute the matrix for all QCed subjects' movie data (~ 800 subjects each group); things were not going well because (1) those matrices are huge, (2) dask computing had some problems, and (3) still takes a long time even with dask
- Then I found something inconsistent; the stimuli lengths are 3.4 mins (TP) and 10 mins (DM), each TR = 0.8 second, how could TP end up with 250 TR? and some subjects even have shorter TRs (248 TR); I check other papers with HBN movie data, they mentioned TP has 201 seconds. Here is the plan:
  - we will use DM data since the information is clearer also longer TRs are better for our eFC
  - I'm debating about whether to trim the first 5-10TR or so before computing eFC...
  - I need to get next steps code ready this weekend while waiting for the first-step computing to be done

### 10/09/2023 - 10/13/2023
- Subjects filteration/selection has done, see [here](https://github.com/sensein/hbn_adhd/blob/main/code/01_select_subjects.ipynb)
- Decide to get cofluctuation matrix for each subject in the qualified QC list regardless of their ADHD diagnosis. The reason is that the computation is quite heavy and if we later (after OHBM) want to include more subjects, grouping them by 3 ADHD subtypes is not logically friendly to append new data (anyway, after many failed trials I decide to compute everything...)
- The parcel-level (we use Scheafer 400-parcel 17 network) pairwise cofluctuation (shape: n_parcel, n_parcel, n_TR) per subject should be done this Saturday. 
- Created [this cute function](https://github.com/sensein/hbn_adhd/blob/58379ac1fd789e240fd603976b8e16c01466106a/code/utils/__init__.py#L1) to quickly get a given subject's movie data information

### 10/02/2023 - 10/06/2023
- YC and MK met, set up timelines:
    - by 10/13, YC will finish participants selection and MK will double check afterwards
    - by 10/20, YC will get eFC matrix for each participants
    - by 10/27, mixed-effect modeling should be done (if nothing wrong with the eFC matrice)
    - by 11/3, fix any potential errors
    - by 11/10, abstract should be done and sent to SG
- other notes (for abstract only):
    - using movie TP data
    - select participants for 3 groups (combined, inattentive, control), match age, sex if possible
    - if possible, address comorbidity in selection & mix-modeling (if we don't have time for OHBM, we will do it later for the paper)
- some related papers:
  - Faskowitz, J., Esfahlani, F.Z., Jo, Y. et al. (2020). Edge-centric functional network representations of human cerebral cortex reveal overlapping system-level architecture. Nat Neurosci 23, 1644–1654. https://doi.org/10.1038/s41593-020-00719-y
  - Betzel, R. F., Faskowitz, J., & Sporns, O. (2023). Living on the edge: network neuroscience beyond nodes. Trends in Cognitive Sciences. https://doi.org/10.1016/j.tics.2023.08.009 
  - Esfahlani, F. Z., Byrge, L., Tanner, J., Sporns, O., Kennedy, D. P., & Betzel, R. F. (2022). Edge-centric analysis of time-varying functional brain networks with applications in autism spectrum disorder. NeuroImage, 263, 119591. https://doi.org/10.1016/j.neuroimage.2022.119591 
  - Sun, A., Wang, J., & Zhang, J. (2023). Identifying autism spectrum disorder using edge-centric functional connectivity. Cerebral Cortex, 33(13), 8122–8130, https://doi.org/10.1093/cercor/bhad103