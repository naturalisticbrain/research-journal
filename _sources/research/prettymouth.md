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
| **Contributors**| Yibei Chen, Zaid Zada, Gasser Elbanna, Greg Ashby, Satra Ghosh, Sam Nastase* |
| **MIT Project**  | No |
| **SIG Project**  | No |

## Project Updates

**This project has been submitted to OHBN 2023 and presented as a poster in July 2023, Montreal, Canada.**

### 02/19/2024 - 02/23/2024
- since YC lost data, we only plotted the behavioral part this time
- YC will recover/rerun the script to get data back + working on figures for next meeting

### 01/29/2024 - 02/02/2024
- yay, payment issue solved and data collected! haven't got time to check the data yet; will start some work next week.

### 01/22/2024 - 01/26/2024
- card payment has some problems, trying to resolve it next week.
- no meeting, no data, no analysis

### 01/15/2024 - 01/19/2024
- had our first meeting in 2024 (01/18) and decided that we'll finish all analyses for this one by end of Feburary then move to writing and working on the budapest one. finish (analysis done) by May.
- before the meeting YC calculated root mean square (RMS) based on both inter-subject and intra-subject cofluctuation.
- to conclude this project, we need to collect another round of behavioral data (ask participants to press the button whenever they find evidence relevant to the information (paranoia vs. affair) provided), in addition to the one we collected for event segmentation. we talked about how to possibly analyze the data: 
  - separate both behavioral data (the 2nd round, evidence one) and the brain RMS into events (based on the 1st round data collection)
  - think about how intra-subject cofluctuation & its RMS provide additional information to our current story?
- satra offers help for the data collection and i will come up with a detailed analysis plan before the data collection. (naming satra my favoriate person of the 3rd week of 2024)
- the authorship will be updated accordingly.

### 11/17/2023 - 12/01/2023
- pause until Jan 18th, 2024

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