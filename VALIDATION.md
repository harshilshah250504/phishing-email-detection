# Dataset and evaluation review

Checked locally on 19 September 2026. Raw email records are not distributed.

## English dataset

- 38,668 records; seven expected columns present.
- Labels: 21,827 labelled 1 and 16,841 labelled 0.
- 73 missing email bodies.
- One exact duplicate row; 303 repeated body values beyond first occurrences (including missing values).

## Hindi dataset

- 20,000 records; seven expected columns present.
- 10,000 ham and 10,000 spam labels.
- No missing values in the expected columns.
- No exact duplicate rows; 7,570 repeated body values beyond first occurrences.

## Implications

Split equivalent email bodies as groups before evaluating to avoid train/test leakage. Document and confirm the mapping between spam/ham and numeric labels; spam labels do not automatically establish phishing ground truth. Handle missing bodies explicitly. Apply resampling only to training data.

The notebook contains exploratory pipelines, including models fitted to resampled full datasets. Training predictions and SHAP explanations are not independent test-set performance. No end-to-end held-out performance result is claimed here. A complete model reproduction remains pending.

## Execution smoke check — 19 September 2026

The final architecture cell's preprocessing, SMOTE/XGBoost training and SHAP functions completed on 40 synthetic records for each language path (English and Hindi). This checks execution only; it does not measure accuracy on real emails or validate Hindi sentiment quality. No email content was transmitted externally.

Environment: Python 3.12, XGBoost 3.4.1, SHAP 0.52, imbalanced-learn 0.14.2. macOS requires an OpenMP runtime; set up libomp before importing XGBoost.
