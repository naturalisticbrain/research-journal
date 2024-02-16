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

# Shinobi cNeuroMod

## Project Description
Video game playing in a deep scanning [dataset](https://www.cneuromod.ca/)

| | |
| -------------- | ----------------------------- |
| **GitHub Link**  | [Private](https://github.com/yibeichan/shinobi-cnm) |
| **Notion** | [Page](https://www.notion.so/yibeichen/shinobi-026d717a5dee4c49ac1624a44a1b82a5?pvs=4) |
| **Contributors**| Yibei Chen, TBD, Satra Ghosh* |
| **MIT Project**  | Yes |
| **SIG Project**  | Yes |

## Project Updates

### 02/19/2024 - 02/23/2024
- met with satra and had a plan (in the notion page) which needs more time and resource. we decide to do it step-by-step and skip this dataset for CCN.

### 01/29/2024 - 02/02/2024
- finally took a look at the extracted information but then I found something confusing; opened an issue [here](https://github.com/courtois-neuromod/shinobi/issues/41)

### 01/15/2024 - 01/19/2024
- finally extracted `bk2` files (game replay files) to `json` files for the game play outside and inside the fmri; but i need to redo the extraction, it turns out that audio extract is also an option, see [here](https://github.com/courtois-neuromod/shinobi_training/issues/1#issuecomment-1900726304). There are some broken `bk2` files too... a bit sad.
- i'll start visualization next week
- fmri data is put aside at this moment

