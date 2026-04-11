# Sleep Health and Daily Performance

This repository contains a reproducible notebook that explores the **Sleep Health and Daily Performance** dataset and builds a baseline workflow to study relationships between sleep behavior, lifestyle factors, and outcomes such as cognitive performance and sleep-disorder risk.

## Project overview

The notebook follows a practical applied-data-science workflow:

- Download the dataset from Kaggle
- Load and inspect the data schema
- Perform exploratory data analysis (EDA)
- Prepare features and target labels
- Establish a baseline modeling setup for downstream experimentation

## Repository structure

- `sleep_health_dataset.ipynb` — end-to-end notebook (download, loading, EDA, and feature/target preparation)

## Dataset

The dataset is sourced from Kaggle: **Sleep Health and Daily Performance**.

From the notebook run:

- Shape: **100,000 rows × 32 columns**
- Target label (classification): `sleep_disorder_risk`

The dataset includes a mix of:

- Demographics (e.g., age, gender, occupation, country, BMI)
- Sleep metrics (e.g., duration, quality score, REM/deep sleep %, latency, wake episodes)
- Lifestyle factors (e.g., caffeine/alcohol before bed, screen time, exercise, steps, naps)
- Context (e.g., room temperature, weekend sleep difference, season, day type)
- Outcome variables (e.g., cognitive performance score, felt rested, sleep disorder risk)

## Getting started

### Prerequisites

- Python 3.9+
- Jupyter Notebook or Google Colab

Install dependencies:

```bash
pip install -U opendatasets kaggle numpy pandas matplotlib seaborn scikit-learn
```

### Kaggle credentials

The notebook downloads the dataset via `opendatasets`, which uses the Kaggle API. Configure Kaggle credentials before running:

1. Create an API token in your Kaggle account settings (downloads `kaggle.json`).
2. Place it at `~/.kaggle/kaggle.json`.
3. Ensure permissions are set correctly (recommended by Kaggle).

Note: Never commit `kaggle.json` or any API keys to this repository.

### Run the notebook

Open and run all cells:

- Local: open `sleep_health_dataset.ipynb` in Jupyter
- Colab: use the “Open in Colab” badge included in the notebook

## Notes and recommendations

- If you run locally (not in Colab), adjust the CSV path if needed.
- For a more complete baseline, consider adding:
  - a deterministic train/test split
  - preprocessing (categorical encoding, scaling) via a pipeline
  - cross-validation and hyperparameter tuning
  - model interpretability (feature importance / SHAP)
  - a short summary of key EDA findings and modeling results

