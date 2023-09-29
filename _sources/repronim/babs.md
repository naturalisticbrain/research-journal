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

# BABS

**GitHub Links**:
- https://github.com/PennLINC/babs

**Contributors**: Dorota, Chenying

## Project Updates

### 09/25/2023 - 09/29/2023
- SOBP abstract submitted ()
- we found a potential solution to fix the **long filepath problem** but the implementation would be not easy, we plan to fix it before the next major release, see [this issue](https://github.com/PennLINC/babs/issues/138)

### 09/18/2023 - 09/22/2023
- got email from Dave about presenting BABS for SOBP. more details next Thursday

### 08/28/2023 - 09/01/2023
We suspect that the [midthickness problem](https://github.com/PennLINC/babs/issues/138) is probably due to that the long path generated by BABS failed to run properly in freesurfer.

### 08/16/2023-08/24/2023
- Start testing, see [this issue](https://github.com/PennLINC/babs/issues/137) for record. The error 
  ```
  [sqlite query crashed: thread blocked indefinitely in an MVar operation
  CallStack (from HasCallStack):
  error, called at ./Database/Handle.hs:81:40 in main:Database.Handle]
  ```
  is one of those not-helpful ones. Dorota thinks it might be related to OpenMind (some nodes specific). Will be checking and tracking those nodes.
- After many resubmits/failures, I got another error related to `midthickness` node in fmriprep, which I first thought was a freesurfer problem and posted on [Neurostars](https://neurostars.org/t/midthickness0-node-crash-during-fmriprep-23-1-4/26592/5). Later, it turned out that it might still be an BABS problem or an OpenMind problem. Tracked in this [issue](https://github.com/PennLINC/babs/issues/138).