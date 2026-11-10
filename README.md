# Uncertainty-Aware Fairness: reviewer evidence

Start with [UAF_Reviewer_Evidence.ipynb](UAF_Reviewer_Evidence.ipynb). It contains executable calculations, saved outputs, model and audit settings, protected-group counts, all 12 main tables, all 101 technical-companion tables, and the associated figures. It also explains how C1–C4 answer the research questions and what each experiment establishes.

For a reading copy without visible code, download [UAF_Reviewer_Evidence.html](UAF_Reviewer_Evidence.html) and open it in a browser. Expand the companion sections to see their protocols, derivations and exhibits. Equation rendering in the HTML copy may require an internet connection; notebook computation does not.

## Run

Use Python 3.11 in a virtual environment and install the tested dependencies:

```bash
python -m pip install -r requirements.txt
python -m ipykernel install --user --name uaf-review --display-name "UAF review"
```

Open the notebook in Jupyter or another notebook editor, select the **UAF review** kernel, and choose **Restart Kernel and Run All**. Alternatively, execute it directly:

```bash
jupyter nbconvert --to notebook --execute UAF_Reviewer_Evidence.ipynb --ExecutePreprocessor.kernel_name=uaf-review --ExecutePreprocessor.timeout=600 --output UAF_Reviewer_Evidence_rerun.ipynb
```

The notebook is self-contained. Aggregate inputs and figures are embedded, and no account, credentials, patient-level records or external dataset files are needed. Installing packages is the only step that requires access to a package repository. Runtime varies by machine; the recorded clean-folder run completed in about 36 seconds.

## What is checked

- All 68 code cells completed without errors in a fresh temporary directory.
- Seventeen assertion groups passed, including 317 checks against printed numerical cells in main Tables III–XII, using each cell's displayed precision.
- All 234 independent-count family forecasts and 42,000 exact pooled policy decisions are recalculated.
- C2 conditional calculations and an exhaustive small-instance check of the C3 allocation recurrence are executed.
- Matched-method, planning and alternative policy-review summaries are reconstructed from frozen aggregate experiment records.

The notebook distinguishes fresh calculations, reaggregation of recorded experiments, and displayed historical evidence. Displaying a saved table is not a rerun of the experiment that produced it. Historical variants remain labelled separately from the current results.

## Paper agreement and scope

[verification.json](verification.json) records the executed notebook checksum, tested environment, scope and SHA-256 fingerprints of the exact main-paper and companion PDF snapshots checked. The main snapshot is the 10 November 2026 professor-review PDF. If either manuscript changes, repeat the agreement checks before treating this package as aligned with that new version.

Raw cohort extraction, model retraining, full clinical allocation simulations and the original runtime benchmarks are not rerun here. The computational checks do not establish independent validation on new hospitals or prospective clinical benefit. Recorded inconclusive, adverse and sensitivity findings are retained.

No patient-level data are included. Dataset access conditions continue to apply to reconstruction from original clinical records. No reuse licence is granted by this repository.
