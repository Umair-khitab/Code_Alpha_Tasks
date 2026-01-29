# CodeAlpha — Sales Prediction Project

This repository contains an exploratory analysis and modeling notebook that investigates how advertising spend across different channels (TV, Radio, Newspaper) affects product sales, and builds predictive models to forecast sales.

Notebook: [Codealpha_sales_prediction_model.ipynb](https://github.com/Umair-khitab/Code_Alpha_Tasks/new/main/Code_Alpha_Tasks/Codealpha_Sales_Price_Prediction)

Open in Colab: https://colab.research.google.com/github/Umair-khitab/Codealpha_sales_prediction_model/blob/main/Codealpha_sales_prediction_model.ipynb

## Project Overview

Goals:
- Understand relationships between advertising channels and sales.
- Build and compare several regression models to predict sales.
- Provide actionable insights for marketing allocation.
- Demonstrate baseline and advanced modeling approaches.

Models implemented in the notebook:
- Linear Regression (baseline)
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regression (SVR)
- ARIMA (for time-series forecasting experiments)

##Evaluation metrics and comparison
### Model Performance Comparison

| Model                  | MAE    | MSE    | R² Score |
|-------------------------|--------|--------|----------|
| Linear Regression       | 1.461  | 3.174  | 0.899 |
| Random Forest           | 0.620  | 0.591  | 0.981 |
| Gradient Boosting       | 0.619  | 0.533  | 0.983 |
| Support Vector Regression (SVR) | 1.162  | 2.862  | 0.909 |
| ARIMA                   | Trained (order=(1,1,1)) | Metrics not reported | Metrics not reported |


## Dataset

The notebook expects a CSV named `Advertising.csv` (the classic advertising dataset: TV, Radio, Newspaper, Sales). Place `Advertising.csv` at the path referenced by the notebook (by default the notebook reads `/content/Advertising.csv` when run in Colab, or `./Advertising.csv` when run locally after updating the path).

If the dataset is not present, download or add it to the repository/data folder before running the notebook.

## How to run

Option A — Run in Google Colab (recommended for quick run):
1. Click the "Open in Colab" link above.
2. Upload `Advertising.csv` to Colab or modify the notebook to load the dataset from a mounted Google Drive.

Option B — Run locally:
1. Clone the repository:
   git clone https://github.com/Umair-khitab/Codealpha_sales_prediction_model.git
2. (Optional) Create and activate a virtual environment:
   python -m venv .venv
   source .venv/bin/activate  # macOS / Linux
   .venv\Scripts\activate     # Windows
3. Install dependencies:
   pip install -r requirements.txt
   (If requirements.txt is not present, install manually: `pip install pandas numpy matplotlib seaborn scikit-learn statsmodels jupyterlab`)
4. Place `Advertising.csv` in the repository root (or update the notebook path).
5. Launch Jupyter / JupyterLab and open `Codealpha_sales_prediction_model.ipynb`:
   jupyter lab

## Notebook structure

- Introduction & objectives
- Libraries import
- Data loading and inspection
- Exploratory Data Analysis (scatter plots, pairplot, correlation heatmap, distribution)
- Preprocessing and train/test split
- Model training (Linear Regression, Random Forest, Gradient Boosting, SVR)
- Model evaluation and comparison
- Time-series exploration using ARIMA (if applicable)
- Conclusions and insights

## Results & Insights (summary)
- TV advertising shows the strongest correlation with sales in the dataset.
- Linear regression provides a simple baseline; ensemble methods (Random Forest / Gradient Boosting) often improve predictive performance.
- ARIMA is included for time-series style forecasting experiments, but the dataset must be arranged as a time series for meaningful ARIMA results.
- Use evaluation metrics (MAE, RMSE, R²) to compare models and select the best-performing approach for your business needs.

## Author
Umair Khitab — Data Science Internship / CodeAlpha project

```
