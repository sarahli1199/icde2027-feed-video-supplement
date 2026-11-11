# ICDE 2027 Feed-to-Video Supplement

Supplemental code and implementation documentation for **From Feed to Video:
Coordinating Multi-Scenario Recommendation with Stackelberg Games**.

Authors: Wenjing Li, Jiang Rong, Zhenzhe Zheng, and Fan Wu.

## Download and read

- [Complete supplemental package](Li_ICDE_Supplement.zip)
- [Supplement PDF](Li_ICDE_Supplement.pdf)
- [Detailed artifact guide](README.txt)
- Known implementation and reproducibility limitations: `docs/KNOWN_ISSUES.txt` inside the ZIP

## Contents of the complete ZIP

- `code/legacy/`: twelve unchanged implementation and plotting scripts.
- `code/verify_artifacts.py`: scoped syntax, integrity, and module checks.
- `docs/`: input schema, source provenance, and known issues.
- `requirements.txt`: versions observed in the local check environment.
- `verification/checks.txt`: the checks actually performed and their scope.
- LaTeX source and the IEEE class needed to compile the supplement.

**No dataset files, model checkpoints, or private industrial logs are included.**
The input schema documents field names only. This repository makes no promise
of a later data release.

## Verification

Download and extract `Li_ICDE_Supplement.zip`, then run from the extracted
`Li_ICDE_Supplement` folder:

```sh
python3 code/verify_artifacts.py
```

This checks Python syntax, source hashes, unresolved local imports, and exclusion
of data/checkpoint files. It does not train models or reproduce the reported
experiments. Existing unresolved imports and evaluation discrepancies are
listed in the known-issues document.

Optional runtime module checks:

```sh
python3 -m pip install -r requirements.txt
python3 code/verify_artifacts.py --runtime
```

The runtime checks use small in-memory tensors; they do not distribute or load
industrial data. Several legacy experiment scripts load private files and
start training at import time. Read the artifact guide and known issues before
running them.

## Reproducibility scope

This repository is an implementation snapshot, not a certified reproduction of
the paper's tables. The original scripts are preserved unchanged. Missing
helpers, differences in evaluation settings and metric branches, and absent
final-run provenance remain documented. The verification utility was written
for artifact inspection and was not used to generate the original results.
