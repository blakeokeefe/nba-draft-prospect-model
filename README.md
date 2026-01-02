# nba-draft-prospect-model

Predicts and ranks NCAA prospects by projected NBA impact using per-40 and advanced efficiency metrics.

## Project Goal
Build a model that ranks draft-eligible NCAA players based on a historical relationship between NCAA performance and normalized NBA success.

## Data
- NCAA per-40 and advanced stats (Sports-Reference)
- NBA outcomes (Basketball-Reference)
- Training sample: 2010–2021 first-round NCAA draftees

## Target Variable
NBA success is measured as **VORP percentile within draft class** (normalized within each draft year).

## Modeling
- Ridge Regression (selected via 5-fold cross-validation)
- Metrics: MAE and Spearman rank correlation (ranking quality)

## Results
- Ridge CV: MAE ≈ 0.245 ± 0.017
- Ridge CV: Spearman r ≈ 0.215 ± 0.10

## Outputs
- `outputs/top30_big_board.csv` — model-ranked prospect board

## How to Run
1. Install requirements:
   ```bash
   pip install -r requirements.txt

