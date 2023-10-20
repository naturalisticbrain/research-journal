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

# Budapest

## Project Description
Hierarchical encoding models in the brain during movie-viewing

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private](https://github.com/yibeichan/event_segmentation_tgbh) |
| **Collaborators**| Zaid Zada, Jeff Mentch, Ron Rice, Sam Nastase* |
| **MIT Project**  | No |
| **SIG Project**  | No |

## Project Updates

**This project has been submitted to SfN 2023 and will be presented as a poster in November 2023, Washington DC, USA.**

### 10/16/2023 - 10/20/2023
- We did find some errors in removing confounds in cifti files; then we did single-subject comparison using old nifti, cifti, new nifti on ridge regression with GPT-2 embedding; ranking from good to bad: old nifti > cifti > new nifti (SN). Because the original fmri data was in 3x3x3.5mm space while cifti and new nifti are in isotopic 2mm space so we decided to rerun fMRIPrep without resampling the brain...it's happening
- While waiting for fMRIPrep to be done, we can start coding for HMM (hopefully done this weekend)

### 10/09/2023 - 10/13/2023
- Encoding models (6 in total) were almost done; but then we found the results suspicious — STS has super high activation across all models, even the messy ones; we had the results from the old fmri data as a baseline; need to double check what happened in this newly preprocessed data before we proceed to the next step.

### 10/02/2023 - 10/06/2023
- finally bring this back to the agenda, TODOs for next week
  - finish post-fmriprep
  - set up four encoding modes
  - compute cofluctuations

### 09/25/2023 - 09/29/2023
- Jeff finished the fmriprep for both datasets
- the rest of us still didn't get time to discuss this project yet...

### 08/24/23
Met with SN; TODOs for the coming week:
- YC figure out previous RA rating data; if not useful, we need to collect new data.
- YC figure out audio feature extraction

### 02/2023—08/2023
YC, ZZ, RR, & SN initialized the project (02/2023)