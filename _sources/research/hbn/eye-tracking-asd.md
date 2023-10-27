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

# Eye-Tracking ASD

## Project Description
Explore the heterogeneity/idiosyncrasy within the ASD group through eye-tracking and phenotype data.

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private on SIG](https://github.com/sensein/eye-tracking-asd) |
| **Collaborators**| Fabio Catania, Jeff Mentch, Satra Ghosh* |
| **MIT Project**  | Yes |
| **SIG Project**  | Yes |

## Project Updates

### 10/23/2023 - 10/27/2023
- met with JM & FC (FC has more detailed notes)
  - we decided to go with movie WK first given that it has real people/faces and faster scene change
  - features: low-high visual features (can be extracted layer by layer) + audio features (TBD)
  - no spatial coordinates from JM's tool
  - we need a sprint for this project, maybe right after SfN/OHBM

### 10/16/2023 - 10/20/2023
- FC & YC met on 10/19, discussed & planned things based on our meeting with SG on 10/18
- FC has emailed Andrea
- planing meetings with JM next week for discussing movie choice, feature choices, & DICE
- YC will put more effort to this after OHBM submission

### 10/02/2023 - 10/06/2023
- YC proposed to separate the methods part out as a new project; no follow-up yet
- YC and FC met and YC will make some plots based on the coordinates in two weeks (not guaranteed given YC's schedule)

### 09/18/2023 - 09/22/2023
- YC and FC met on Thursday and splitted the task for writing pre-registration. Next meeting will be on 10/05.

### 09/11/2023 - 09/15/2023
- We discussed the behavioral encoding model with Satra on Thursday, then we decided to do pre-registration

### 09/05/2023 - 09/08/2023
- got metadata for eyetracking (e.g., sampling rate (subjects have different sampling rates), starting, ending time, order)
- subtracted the starting time from the eyetracking record, then I got negative numbers for the first couple of lines in each file (I haven't figured out why yet)

### 08/28/2023 - 09/01/2023
- Revised my behavioral data cleaning code from last week
- Reformatted the eyetracking txt into multiple CSV files (e.g., fixation, saccade, blink, etc.).
- Figured out the actual starting & ending time for the eyetracking data! Haven't extracted it yet but will do it next week! Then we can start playing with the data...

### 08/23/2023 — 08/24/2023
- Cleaned the eye-tracking data with behavioral information, figured out who has watched which movie(s) in what order.
- Met with Fabio for next steps:
  - YC will extract time series data from eye-tracking txt. I need to **feel** the data to come up concrete/interesting RQs. 
  - FC will explore the phenotype data and the stimuli. We may need to coordinate with MK and JM at some point.

### 08/17/2023
First meeting with Fabio, agreed on the goal of this project: Explore the heterogeneity/idiosyncrasy within the ASD group. Specifically:
- we will do ASD vs TD comparison as the baseline checking
- our focus will be within ASD group


