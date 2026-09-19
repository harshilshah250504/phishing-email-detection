# Multilingual Phishing Detection

English and Hindi email-classification experiments using engineered features, XGBoost, SMOTE, and SHAP.

## Status and prerequisites

The original datasets are required: Cleaned_English_Dataset.xlsx and hindi_emails_merged.xlsx (some experiments reference a CSV variant). They are not included. Update the /content/ paths to your dataset location. WHOIS domain checks may need internet access. Contains multiple experimental pipelines and repeated function definitions; inspect cells before running. Model performance has not been independently reproduced.

Saved outputs and notebook session metadata have been removed. Dependencies are inferred from imports; a fully reproduced environment and pinned versions are pending.

## Setup

```sh
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab notebooks/phishing-email-detection.ipynb
```

## Author

Harshil Prashant Shah · [Portfolio](https://harshil-prashant-shah.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/harshilpshah/)

## Local dataset configuration

See [DATA_SETUP.md](DATA_SETUP.md). Required datasets have been located in the author’s local materials and remain excluded from GitHub. The notebook now uses `PROJECT_DATA_DIR` or the local `data/` directory instead of fixed Colab paths. Full pipeline validation is still in progress.

## Research reference

[Paper on IEEE Xplore](https://ieeexplore.ieee.org/document/11566454) — project reference supplied by the author. Publisher or Drive access conditions may apply.

## Dataset review

See [VALIDATION.md](VALIDATION.md) for locally checked row counts, missing values, duplicate content, and evaluation limitations.
