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

# Data Processing

## Project Description
Pre & post processing image (fMRI) data.

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private on SIG](https://github.com/sensein/hbn_fmri) |
| **Collaborators**| Jeff Mentch, Steven Meisler, Maedbh King|
| **MIT Project**  | Yes |
| **SIG Project**  | Yes |

## Project Updates

fmriprep is done for all 1-10 releases data. 2864 out of 3311 subjects are successful.

### 09/18/2023 - 09/22/2023
- mriqc is running (1483 to be done by Friday or Saturday)

### 09/05/2023 - 09/08/2023
- keep (re)running resting state data for release 10 (kep failing for disk quota reason but I got ~100 more subjects done this week, still 300-400 subjects to go)
- all movie data is finished so I used the xcp-d qc output to take a quick look at FD.
  - movie_DM: 1822 out of 2290 subjects meanFD < 0.2mm
  - movie_TP: 1951 out of 2344 subjects meanFD < 0.2mm
  - note: FD > 0.2 mm is considered as high motion [^1] 
  - need to take a deeper look at other qc measures provided by xcp-d.

### 08/28/2023 - 09/01/2023
- Started the GitHub repo on SIG with Jeff to document code & record successful/failed subjects
- Realized that I only ran fmriprep + xcp-d on movie data, now running the pipeline on the resting state data
- Met with Jeff on Monday discussing plans after fmriprep + xcp-d, mostly we need to come up with quality control measures/assessments so that we can filter out unqualified data for further analysis. This is different from MRIQC because (1) we didn't run MRIQC before fMRIPrep, which we should ... and (2) our assessments are more naturalistic analysis focused; for people who want to run other type of analyses, they can come up with their own customized assessments.

### 08/25/2023
The second round of fmriprep + xcp-d finished with mixed sucess, two major errors found:
- `mkdir: write error: Disk quota exceeded` 
  - -> cleaned my `tmp` folder and rerun those subjects.
- `slurmstepd: error:.*DUE TO TIME LIMIT*`
  - -> I'll fix this once I fix all other errors.

### 08/21/2023
After this first round (I call it first round because all subjects were submitted simultaneously, but this is almost my 5th or 6th times running the same script on them), two major errors found:
- `ValueError: Only one phase-encoding direction <j-> found across sources.` 66 subjects missing the other PE direction `j` file. 
  - -> rerun fmriprep with `--ignore fieldmaps`. I tried `--use-syn-sdc`, which still gave me the same error
- `slurmstepd: error:.*DUE TO TIME LIMIT*` those subjects (n=21) were stuck at `resume recon-all`
  - -> I guess I will give them another chance. If the same, I'll just let them go
- I do see some other minor errors during xcp-d, which don't make too much sense to me at this point, I will deal with them during the final round.

[^1]: Power, J. D., Barnes, K. A., Snyder, A. Z., Schlaggar, B. L., & Petersen, S. E. (2012). Spurious but systematic correlations in functional connectivity MRI networks arise from subject motion. Neuroimage, 59(3), 2142-2154. https://doi.org/10.1016/j.neuroimage.2011.10.018.