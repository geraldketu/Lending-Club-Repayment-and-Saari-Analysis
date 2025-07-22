# Lending Club Loan Repayment Prediction
## Overview

This project explores loan repayment patterns in the Lending Club dataset and applies machine learning and financial analysis techniques inspired by Saari’s framework. It is organized into two Jupyter notebooks:

- **Part1.ipynb** – Data cleaning, exploratory analysis, feature engineering, and model training (Logistic Regression & Random Forest) to predict whether a borrower will fully repay their loan.  
- **Part2.ipynb** – Financial decomposition and Saari‑inspired diagnostics on cash‑flow and repayment trajectories.

## Project Structure

├── Part1.ipynb # ML pipeline: load data, preprocess, train & evaluate classifiers
├── Part2.ipynb # Financial analysis module: cash‑flow breakdown & Saari metrics

## Key Features

- **Data Preparation**
  - Handling mixed‑type columns and missing values
  - Encoding categorical variables for model input

- **Modeling & Evaluation**
  - Train‑test split and baseline hyperparameter settings
  - Logistic Regression and Random Forest classifiers
  - Performance metrics: accuracy, F1 score, ROC curve, and AUC

- **Financial Analysis**
  - Cash‑flow timeline visualization
  - Application of Saari’s mathematical lens to repayment patterns

## Getting Started

### Prerequisites

- Python 3.8 or higher  
- Jupyter Notebook or JupyterLab  
- `pandas`, `matplotlib`, `scikit-learn`

### Dependencies
```bash
pip install pandas matplotlib scikit-learn
```
### Dependencies
Part 1 yields a classification report with precision, recall, F1 score, and ROC AUC for both models.

Part 2 visualizes principal vs interest flows and introduces a novel Saari metric for profiling loan trajectories.

