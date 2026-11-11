SUPPLEMENT: CODE AND IMPLEMENTATION DOCUMENTATION

Paper: From Feed to Video: Coordinating Multi-Scenario Recommendation
       with Stackelberg Games

The main paper remains 12 pages plus references. This is a separate supplement.
No data files, synthetic datasets, model checkpoints, or industrial result logs
are included. No data-availability or release promise is made.

Contents
  Li_ICDE_Supplement.pdf / .tex  Supplementary implementation and artifact guide
  IEEEtran.cls                 Supplied IEEE class, unchanged
  code/legacy/                 12 unchanged implementation/plotting scripts
  code/verify_artifacts.py      New, limited packaging and module-check utility
  requirements.txt             Versions observed in the local check environment
  docs/PROVENANCE.txt           Source-relative origins and SHA-256 checksums
  docs/DATA_SCHEMA.txt          Input fields only; no records
  docs/KNOWN_ISSUES.txt         Known execution and manuscript-alignment gaps
  verification/checks.txt       Results of the scoped checks actually performed

Start here
  Read the supplement PDF and docs/KNOWN_ISSUES.txt before running experiments.
  The archived scripts are not certified to reproduce the paper's tables.
  Several scripts load data and begin training at import time.

Code checks without installing ML dependencies
  python code/verify_artifacts.py

Optional runtime module checks (does not load industrial data or train models)
  python -m pip install -r requirements.txt
  python code/verify_artifacts.py --runtime --report verification/checks.txt

Compile the supplement
  tectonic Li_ICDE_Supplement.tex
  or run pdflatex Li_ICDE_Supplement.tex twice.

Historical experiment entry points
  SGD.py, Mirror_descent.py, bi_level.py, Base_MARL.py, Hierarchical_RL.py,
  Causal_Inference.py, ablation_study.py, and jev_stackelberg_comparison.py
  are archived in code/legacy/. They require the private input CSVs and,
  for some entry points, missing helper functions. They use different
  working-directory assumptions; see the supplement and issue notes.

Provenance and verification scope
  The original project README contains the same reported Feed CTR improvements
  (20.00%, 7.59%, 5.06%) and JEV+ improvements (19.74%, 17.90%, 23.94%) as
  the paper. This supports the project's relevance but does not identify the
  exact code revision, seeds, data split, or run behind each reported number.
  The original code has been preserved, including known limitations; no silent
  scientific or evaluation fixes have been made. The verification utility is
  newly written and was not used to produce the submission's original results.

Submission status
  This is an organized artifact snapshot and accompanying documentation.
  Author review and resolution of the documented reproducibility gaps are
  needed before treating it as a complete, executable reproduction package.

Single-blind author information
Authors: Wenjing Li, Jiang Rong, Zhenzhe Zheng, Fan Wu.
Affiliations and all four email addresses match the main manuscript.
ORCID icons link from each author name: Wenjing Li 0009-0003-1721-1832;
Jiang Rong 0009-0001-0953-8865; Zhenzhe Zheng 0000-0002-5094-5331;
Fan Wu 0000-0003-0965-9058. PDF metadata lists the four current authors.

Documentation split
The two-page supplement retains inventories, compact single-column tables,
commands, and detailed artifact limitations. Model interfaces, training/ranking
defaults, input processing, metric behavior, and verification scope are explained
in Section VIII of the 12-page main paper. Code, requirements, provenance,
data-schema documentation, known-issue notes, and recorded checks are unchanged.

LaTeX uses the standard orcidlink package for the linked iD icons.
