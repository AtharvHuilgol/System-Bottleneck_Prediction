---
description: Run the bottleneck prediction model pipeline
---

# Bottleneck Prediction Model — Workflow

// turbo-all

## Prerequisites

Install the required Python packages (only needed once):

```
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

## Running the Pipeline

1. Open the notebook in VS Code or Jupyter:

```
cd "D:\Education\PCCOE\Academics\Data Science Mini Project"
jupyter notebook bottleneck_model.ipynb
```

2. Run all cells sequentially (Kernel → Restart & Run All), or run each stage one-by-one:

   - **Stage 0**: Imports all libraries
   - **Stage 1**: Loads dataset and performs EDA (class distribution, correlation heatmap, feature distributions)
   - **Stage 2**: Splits data 80/20 (stratified) and applies StandardScaler
   - **Stage 3**: Applies SMOTE to balance the training set (99:1 → 1:1)
   - **Stage 4**: Trains 4 models: Logistic Regression, Random Forest, XGBoost, SVM
   - **Stage 5**: Evaluates models with classification reports, confusion matrices, ROC curves; selects the best model by Bottleneck F1-score
   - **Stage 6**: Predicts bottleneck points on the full dataset, generates scatter plots and feature importance chart

3. All output plots are saved automatically to the `results/` folder.

## Output Files

After running, the `results/` folder will contain:

| File | Description |
|---|---|
| `01_class_distribution.png` | Bar & pie chart of Working vs Bottleneck counts |
| `02_correlation_heatmap.png` | Feature correlation matrix |
| `03_feature_distributions.png` | Histograms of all features by class |
| `04_smote_balance.png` | Before/after SMOTE class balance |
| `05_confusion_matrices.png` | Confusion matrices for all 4 models |
| `06_roc_curves.png` | ROC curves with AUC scores |
| `07_bottleneck_scatter.png` | Scatter plots showing predicted bottleneck points |
| `08_feature_importance.png` | Feature importance from best model |

## Interpreting Results

- **Best model** is selected by the highest F1-score on the Bottleneck class
- The final cells display all predicted bottleneck points with their feature values
- The feature importance plot shows which system metrics contribute most to bottleneck prediction
