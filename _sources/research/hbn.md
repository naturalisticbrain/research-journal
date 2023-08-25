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

# Healthy Brain Network

## Project Description
[Describe your project here]

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | None |
| **Collaborators**| People at SIG          |
| **MIT Project**  | Yes                    |
| **SIG Project**  | Yes                    |


## Project Updates

### 1. Preprocessing

**Code on GitHub**: [Private](https://github.com/yibeichan/hbn_practice/tree/main/fmri/code)

I am running fmriprep and xcp-d on release 10 subjects. Jeff is taking care of releases 1-9.

There are 700 subjects in total.
- 45 subjects do not have either `func` or `anat`, should be excluded.
- 3 subjects miss `fmap` but not other parts, should be fmriprepped with `--ignore fieldmaps`


@08/21/2023
> After this first round (I call it first round because all subjects were submitted simultaneously, but this is almost my 5th or 6th times running the same script on them), two major errors found:
> - `ValueError: Only one phase-encoding direction <j-> found across sources.` 66 subjects missing the other PE direction `j` file. 
> - - -> rerun fmriprep with `--ignore fieldmaps`. I tried `--use-syn-sdc`, which still gave me the same error
> - `slurmstepd: error:.*DUE TO TIME LIMIT*` those subjects (n=21) were stuck at `resume recon-all`
> - - -> I guess I will give them another chance. If the same, I'll just let them go
> - I do see some other minor errors during xcp-d, which don't make too much sense to me at this point, I will deal with them during the final round.

@08/25/2023
> The second round of fmriprep + xcp-d finished with mixed sucess, two major errors found:
> - `mkdir: write error: Disk quota exceeded` 
> - - -> cleaned my `tmp` folder and rerun those subjects.
> - `slurmstepd: error:.*DUE TO TIME LIMIT*`
> - - -> I'll fix this once I fix all other errors.

### 2. Eye-tracking

```{include}eye-tracking-asd.md
```

### 3. ReproSchema

```{include}../repronim/reproschema.md
```
