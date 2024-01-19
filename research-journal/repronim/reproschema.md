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

# ReproSchema

**GitHub Links** 
- https://github.com/ReproNim/reproschema
- https://github.com/ReproNim/reproschema-library

## Project Updates

**Manuscript draft internal deadline: Feb. 2nd, 2024**

**Major updates deadline: Jan. 5th, 2024**

---
**Manuscript**
### 12/26/2023 - 01/19/2024
- draft has been revised a couple of rounds but the `user cases` section is still to-be-written. this section will include `hbcd`, `bridge2ai`, `nimh-minimal`. i need to come up with a 
- software side: working on improving the `redcap2reproschema` tool based on `hbcd` and `bridge2ai`
  - `hbcd`: got the data dictionary using redcap API, but haven't figured out how to retrive historical versions yet
  - `bridge2ai`: we start a thread with evan and alistir, will have more updates next week
  - `nimh-minimal`: we have some javascript bugs in `ui` needs to be fixed, haven't been fixed yet
- set up a meeting with MIT writing center to go through the draft on Jan. 26th (next Friday)

### 12/04/2023 - 12/08/2023
- draft progress:
  - Intro (95% done)
  - Reproschema Description/Design and Functionality (90% done)
  - Component Overview (90% done)
  - Comparative Analysis (the [table](https://docs.google.com/spreadsheets/d/1JGlxDM1NS0wO3eaqc3yK-roFxJcWVtvhIhUWjNyMiME/edit?usp=sharing) (SG & YC access only) is done but other text part hasn't started yet)
  - Practical Walkthrough (will start next week)
  - Discussion (not started yet)

### 11/17/2023 - 12/01/2023
- finally I got redcap account
- met with Satra and set up plans
  - manuscipt done by the end of the year

---
**Package Maintainance**
### 01/11/2024 - 01/12/2024
- EAB meeting:
  - `reproschema-protocol-cookiecutter` done
  - `reproschema-demo-protocol` done
  - `redcap2reproschema` done
  - `reproschema2redcap` done
  - `reproschema online document` done
  - `LinkML conversion` not done
- After EAB meeting TODOs:
  - `nimh-minimal` needs to be finalized, which requires some fixes in `ui`
  - improve `reproschema-protocol-cookiecutter` by enabling users to directly add activities from `reproschema-library`

### 12/04/2023 - 12/08/2023
- met with Dorota on 12/07
  - aim to finish LinkML part next week
  - where to put the pytantic layer (decide next week)
- YC works on demo/walkthrough next week

### 11/17/2023 - 12/01/2023
- met with Satra and set up plans
  - new release with linkML should be done in December
  - using linkML to convert reproschema to redcap (current script used javascript)
- will meet with Dorota discussing next steps Dec. 5th

---
**Converting HBN assessments**

**Code on GitHub**: [Private](https://github.com/yibeichan/hbn_practice/tree/main/reproschema)

**Contributors**: Dorota, Kseniia, Maedbh, Sooyang, etc.

### 10/16/2023 - 10/20/2023
- had a meeting with Dorota & Sooyang discussing about where we are at with LinkML
- Dorota & Sooyang will keep working on this next Monday, YC will catch up on this after OHBM submission

### 09/25/2023 - 09/29/2023
- got some feedback on other comparable tools (added to the outline) at the repronim meeting
- fix abcd_cbcl01 scoring, see [PR](https://github.com/ReproNim/reproschema-library/pull/68)

### 09/18/2023 - 09/22/2023
- drafted the outline for manuscript, DJ has commented on it.

### 09/11/2023 - 09/15/2023
- played with the [demo-protocal](https://github.com/yibeichan/demo-protocol), got some errors for loading the webpage

### 09/05/2023 - 09/08/2023
- DJ and YC went through YC's PR and then merged it
- YC will use the newly added assessment to create a protocol (via reproschema-ui repo). This would be useful for
  - testing whether the assessments works
  - checking whether the reproschema-ui documentation needs any improvement
  - writing the paper because making this protocal can help us to put our feet into user's shoes to see what kind of obstacels they would ecounter, etc.

### 08/28/2023 - 09/01/2023
- Revised the 12 assessments in this [PR](https://github.com/ReproNim/reproschema-library/pull/67) 

### 08/24/2023
- Start (manually) collecting free HBN assessments, shared on [SIG Google Drive](https://drive.google.com/drive/folders/19WaMiDkIfXoBbIP4DfMj57j0Q9IHq2E-?usp=drive_link). Kseniia has access too.
- We can't calculate subscores for CBCL, because it's not free. We can't make it public either. This applies to all private/paid assessments. (Kseniia)
- Dorota and I will review this [PR](https://github.com/ReproNim/reproschema-library/pull/67) on 08/29/2023.

### 07/2023
- Start converting HBN assessments to reproschema library; Maedbh provided cleaned items
- Maedbh introduced Kseniia
- Dorota has been helping with programing.

