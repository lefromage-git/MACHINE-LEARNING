# MACHINE-LEARNING

Lab work for **TEB3123 Machine Learning**, Universiti Teknologi PETRONAS.

**Student:** Muhammad Aqil Bazli Bin Jafni

## Repository structure

```
MACHINE-LEARNING/
├── all_datasets/          # CSV datasets provided for the labs
├── all_experiments/       # one Jupyter notebook per lab + helper scripts
│   ├── lab01_feature_engineering.ipynb
│   ├── lab02_supervised_learning.ipynb
│   └── predict_passenger.py
├── models/                # models saved by the notebooks (joblib + model card)
├── requirements.txt
└── README.md
```

The notebooks set `PROJECT_ROOT = Path.cwd().parent`. That means they must be **run from inside `all_experiments/`**. Datasets are then read from `../all_datasets` and models are saved to `../models`.

## Labs

| Lab | Topic | Notebook | Highlights |
|---|---|---|---|
| 1 | Feature engineering and feature selection | [lab01_feature_engineering.ipynb](all_experiments/lab01_feature_engineering.ipynb) | Titanic features (title, family size, log fare), scaling and distances, SelectKBest / lasso, leakage demo |
| 2 | Supervised learning I: regression, classification, and the workflow | [lab02_supervised_learning.ipynb](all_experiments/lab02_supervised_learning.ipynb) | OLS vs ridge, chronological validation, thresholds, grid-search CV, saved Titanic model, heart-failure exercise, threshold memo |

Each notebook also includes the lab's **Try it yourself** exercise, plus answers to the **Check your understanding** questions. Lab 2 also includes the **Decision memo**.

## How to run

```bash
pip install -r requirements.txt
cd all_experiments
jupyter notebook
```

Use the saved Titanic model from the terminal. Run Lab 2 first so that `models/` exists:

```bash
cd all_experiments
python predict_passenger.py --pclass 2 --sex female --age 30 --fare 20
```
