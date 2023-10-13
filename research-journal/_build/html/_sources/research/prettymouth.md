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

# Prettymouth

## Project Description
Belief-dependent cortical network dynamics during naturalistic audio-listening

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private](https://github.com/yibeichan/prettymouth) |
| **Collaborators**| Zaid Zada, Gasser Elbanna, Greg Ashby, Sam Nastase* |
| **MIT Project**  | No |
| **SIG Project**  | No |

## Project Updates

**This project has been submitted to OHBN 2023 and presented as a poster in July 2023, Montreal, Canada.**

### 10/09/2023 - 10/13/2023
- We didn't discuss/do any work on this project this week but the preprocessing issue from `budapest` reminds us to check the preprocessed data as well since those two projects use the same fmriprep + post-fmriprep code.

### 10/02/2023 - 10/06/2023
- well, YC's methods got pushed back
- prompts for behavioral data approved, but I currently don't have time to set up Pavlovia for data collection
- We need to shift our focus to the SfN project so we have to slow this one down a bit; not a pause
- Gonna make some plots SN wants

### 09/25/2023 - 09/29/2023
- add network analyses
- prepare prompts for new behavioral data collection
- writing writing writing!!!

### 09/18/2023 - 09/22/2023
- YC need to update plots/figures
- new concerns raised. 
  - we need behavioral ratings for each event (how to get it?)
  - we need to do some network-level analysis

### 09/11/2023 - 09/15/2023
- disagreement resolved, move to plotting and manuscript writing

### 09/05/2023 - 09/08/2023
- SN and YC have disagreement on processing the behavioral event boundary data
- ZZ and SN suggested different methods on detecting peaks
- YC will run analysis again this Sunday

### 08/28/2023 - 09/01/2023
- `--use-aroma` is depricated since fMRIPrep 23.1.0
- We go for `cifti` format
- Cofluctuation calculation ready for all parcel versions
- TODOs:
  - finish the behavioral event segmentation analysis
  - keep writing the methods part while doing the analysis

### 08/24/2023
Met with SN; TODOs for the coming week:
- new fmriprep + preproc data ready (from GE). But I need to check what `--use-aroma` did. SN is concerned about `--output-spaces MNI152NLin6Asym:res-2 anat `; we should be more cautious when modifying the original BOLD signals (minimize the resampling on BOLD as much as possible).
- I need to figure out `cifti` format and rerun our previous analyses.
- Prolific data collection completed! Within 3 hours! Now I need to figure out how to analyze it.
- Thinking about how to create Figure 1 (schematic).
- Keep revising the intro part.

### 03/2022—08/2023
- YC and GA initalized the project (03/2022)
- YC invited SN (08/2022)
- SN invited ZZ (10/2022)
- YC invited GE (08/2023)