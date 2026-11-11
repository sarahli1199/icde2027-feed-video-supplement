# ICDE 2027 Feed-to-Video Supplement

Supplemental code and implementation documentation for **From Feed to Video:
Coordinating Multi-Scenario Recommendation with Stackelberg Games**.

Authors: Wenjing Li, Jiang Rong, Zhenzhe Zheng, and Fan Wu.

## Download and read

- [Complete supplemental package](Li_ICDE_Supplement.zip)
- [Supplement PDF](Li_ICDE_Supplement.pdf)
- [Detailed artifact guide](README.txt)
- Implementation and reproducibility limitations: Section IV of the supplement PDF

## Contents of the complete ZIP

- `code/legacy/`: twelve implementation and plotting scripts using generic input names.
- `requirements.txt`: versions observed in the local check environment.
- LaTeX source and the IEEE class needed to compile the supplement.

**No dataset files, model checkpoints, or private industrial logs are included.**
The code uses generic semantic column names and input filenames. No internal
schema or name mapping is included. This repository makes no promise of a later
data release.

## Using the artifacts

Download and extract `Li_ICDE_Supplement.zip`. Read the included artifact guide
and Section IV of the supplement PDF before running the archived scripts. Dependencies
can be installed from the extracted `Li_ICDE_Supplement` folder:

```sh
python3 -m pip install -r requirements.txt
```

The experiment entry points are in `code/legacy/`. They require private input
files and, in some cases, missing helper functions. Several scripts load those
files and start training at import time. Installing the dependencies alone does
not resolve these limitations.

## Reproducibility scope

This repository is an implementation snapshot, not a certified reproduction of
the paper's tables. Input identifiers and filenames have been generalized;
algorithmic logic and numeric settings are retained. Missing
helpers, differences in evaluation settings and metric branches, and absent
final-run provenance remain documented in the supplement PDF and main paper.
