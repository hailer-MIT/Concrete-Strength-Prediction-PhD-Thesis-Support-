# Concrete Strength Predictor Using Random Forest

## Problem Statement

Civil engineers often require reliable estimates of concrete compressive strength to optimize building designs. However, lab testing is expensive and time-consuming. This project presents a machine learning approach to predict compressive strength from component proportions.

## Solution

Using historical concrete mix data, a **Random Forest Regressor** was trained to predict the compressive strength with high accuracy. The model allows engineers to simulate and test different mix combinations virtually before implementation.

## Technical Approach

1. **Data Loading** – CSV input with 8 features: Cement, Slag, Fly Ash, Water, Superplasticizer, Coarse Aggregate, Fine Aggregate, Age.
2. **Preprocessing** – StandardScaler applied to normalize features.
3. **Modeling** – RandomForestRegressor trained with 80/20 train-test split.
4. **Evaluation** – Metrics include MAE, RMSE, and R².
5. **Visualization** – Feature importance, heatmaps, and residual analysis.
6. **Model Saving** – Model and scaler saved with `joblib`.

## Results

- **R² Score:** 0.88
- **MAE:** ~3.73 MPa
- **RMSE:** ~5.46 MPa
- **Interpretation:** Model explains ~88% of variance with minimal error – suitable for real-world strength estimation.

## Tools & Libraries

- Python (Pandas, Numpy)
- Scikit-learn
- Matplotlib & Seaborn
- Joblib (for saving model)
- Google Colab (for execution)

## Dataset

- **Source:** UCI Concrete Compressive Strength Dataset
- **Link:** [UCI Repository](https://archive.ics.uci.edu/ml/datasets/concrete+compressive+strength)
- Download and place the CSV file into the `data/` directory or upload it during runtime in Colab.
