# Uncertainty-Aware Fairness

This repository accompanies the paper. The [reviewer notebook](UAF_Reviewer_Evidence.ipynb) presents C1–C4 with executable calculations, saved outputs and explanations of the research questions, methods and findings.

It includes model and audit settings, protected-group counts, all 12 main tables, all 101 technical-companion tables, and the associated figures. The sections follow the study from audit decisions and source sensitivity through evidence allocation and policy review.

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

The notebook is self-contained: aggregate inputs and figures are embedded. After installing the dependencies, execution requires no account, credentials, network connection or external dataset files.

## Notebook contents

Running the notebook recalculates exact count-law probabilities, conditional source quantities, an allocation-algorithm example and exact pooled policy decisions. The remaining tables are reconstructed from included aggregate experiment records; model fits and runtime benchmarks are provided as recorded results.

[manifest.json](manifest.json) lists the package contents, software environment and notebook checksum. No patient-level data are distributed; access to the original clinical datasets remains subject to their providers' conditions.
