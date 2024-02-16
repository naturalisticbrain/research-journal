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
- reproschema: https://github.com/ReproNim/reproschema
- reproschema-library: https://github.com/ReproNim/reproschema-library
- reproschema-py: https://github.com/ReproNim/reproschema-py
- reproschema-ui: https://github.com/ReproNim/reproschema-ui
- reproschema-protocol-cookiecutter: https://github.com/ReproNim/reproschema-protocol-cookiecutter
- reproschema-demo-protocol: https://github.com/ReproNim/reproschema-demo-protocol
- hbcd-schema: https://github.com/sensein/hbcd-schema
- b2ai-redcap2rs: https://github.com/sensein/b2ai-redcap2rs
- nimh-minimal: https://github.com/ReproNim/nimh-minimal

## Project Updates

**Manuscript draft internal deadline: Feb. 2nd, 2024**

**Major updates deadline: Jan. 5th, 2024**

---
## Manuscript 

I include some software development updates here too, since they are associated with the manuscript

### 02/19/2024 - 02/23/2024
- met with Thalia the forth time, we went through the methods/results/discussion based on last week's feedback (I didn't update here last week); making improvements everytime
- keep revising + making figures during the weekend
- plan to meet with Thalia next Friday too

### 01/29/2024 - 02/02/2024
- sent the draft to Satra on Monday but then we have some formatting concerns (in the email); talked to Thalia on Friday, very helpful and I think I have a solution.

### 01/22/2024 - 01/26/2024
- finished the draft, met with Thalia from the writing center, discussed revision directions (01/16). I'll revise the draft sunday and monday then send to Satra and I'll keep revising it while Satra is reading it. Scheduled another meeting with Thalia next Friday.
- 20 minutes zoom with Jonasch was helpful for the usercase
- b2ai-redcap2rs was done for the current 4 versions.
- hbcd-schema has some problems: 
  - my github folder was under icloud so it syncs in real time; the hbcd data dictionary is huge and generates a lot of files for every conversion; i was too fast for "delete old version, copy new version, & git add ." but then by the time i finished typing commit message, both versions appeared in the folder. I didn't realize what happen until later, which means that some tags may have two versions so I want to redo it to make sure things are correct.
  - I notice that for some data dictionary versions, especially when there are 2 version within a month, I couldn't find the differences between two converted versions. By "I couldn't find the differences" I mean I deleted the old one and added the new one git can't notice the changes. I'm thinking my converting tool may have failed to capture certain part of the reproschema so two conversions got the same result. (if I'm making any sense here)
- nimh-minimal: monday i spent the whole day trying to fix the branch logic at the activity level, opened an [issue here](https://github.com/ReproNim/reproschema-ui/issues/320). I'm thinking about adding a new part in `components` to take care of the between activity logic. haven't got time to implment it yet.
- just a reminder to myself: we want to allow users to pull activities directly from the library when you using the cookiecutter

### 12/26/2023 - 01/19/2024
- draft has been revised a couple of rounds but the `user cases` section is still to-be-written. this section will include `hbcd`, `bridge2ai`, `nimh-minimal`. i need to come up with a struture template for usercases.
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
## Package Maintainance
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
## Adding Assessments

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

