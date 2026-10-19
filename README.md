# F1 Podium Prediction — Milestone 1

Predicting whether a Formula 1 driver finishes on the podium (`positionOrder <= 3`) using only information
available **after qualifying and before the race starts**.

The project builds a full pipeline: auditing and cleaning the raw relational F1 tables, answering three
data-engineering questions, building a leakage-safe modelling table (one row per driver per race), and
training and explaining statistical and neural-network models.

## Repository contents

| File | What it is |
|---|---|
| `F1_Podium_Prediction_MS1.ipynb` | The full run-all notebook: audit, cleaning, data-engineering answers, features, models, experiments, XAI, inference |
| `report/` | The analytical report (PDF) |
| `requirements.txt` | Python packages needed to run the notebook |

## Data

Formula 1 World Championship (1950–2024), Kaggle / Ergast:
<https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020>

The CSVs are **not** stored in this repository. The notebook finds them automatically:

- **On Kaggle:** add the dataset to the notebook; no path changes needed.
- **Locally:** download the dataset and put the 14 CSV files in a `data/` folder next to the notebook,
  or set the `F1_DATA_DIR` environment variable to their location.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook F1_Podium_Prediction_MS1.ipynb   # then Kernel → Restart & Run All
```

The raw CSVs are never modified: the notebook fingerprints them at the start and verifies the
fingerprints at the end.

## Kaggle notebook

<https://www.kaggle.com/code/tonyshehata/team-71-formula-1-podium-prediction-milestone-1>

## Team 71

- Tony Hany
- Omar Medhat
- Mina Magdy
- Maged Emil
