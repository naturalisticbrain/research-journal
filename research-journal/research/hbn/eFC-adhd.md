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
| **Collaborators**| Maedbh King, Satra Ghosh* |
| **MIT Project**  | Yes |
| **SIG Project**  | Yes |


## Project Updates
This project is aiming at OHBM 2024 submission (deadline: 11/17/2023)

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