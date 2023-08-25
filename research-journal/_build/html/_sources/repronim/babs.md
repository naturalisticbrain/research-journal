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

| **GitHub Links** | |
| -------------- | ----------------------------- |
| **BABS** | https://github.com/ReproNim/reproschema |
| **Collaborators**| Dorota, Chenying, TBD |

## Project Updates

### 1. Testing fMRIPrep via BABS on OpenMind

@08/16/2023-08/24/2023
> - Start testing, see [this issue](https://github.com/PennLINC/babs/issues/137) for record. The error 
>   ```
>   [sqlite query crashed: thread blocked indefinitely in an MVar operation
>   CallStack (from HasCallStack):
>   error, called at ./Database/Handle.hs:81:40 in main:Database.Handle]
>   ```
>   is one of those not-helpful ones. Dorota thinks it might be related to OpenMind (some nodes specific). Will be checking and tracking those nodes.
> - After many resubmits/failures, I got another error related to `midthickness` node in fmriprep, which I first thought was a freesurfer problem and posted on [Neurostars](https://neurostars.org/t/midthickness0-node-crash-during-fmriprep-23-1-4/26592/5). Later, it turned out that it might still be an BABS problem or an OpenMind problem. Tracked in this [issue](https://neurostars.org/t/midthickness0-node-crash-during-fmriprep-23-1-4/26592/5).