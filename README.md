# System Bottleneck Prediction Model

This repository contains a machine learning pipeline that builds a **binary classification model** to label system states as either **"Bottleneck"** or **"Working"** based on system performance metrics.

## 🚀 Overview

The goal of this project is to accurately detect system bottlenecks using a machine learning model. Because bottleneck states are typically rare compared to normal working states, the dataset presents extreme class imbalance (99% Working vs 1% Bottleneck). We handle this by using SMOTE to balance our training data and leveraging XGBoost for high predictive performance.

## 🗂️ Project Structure

- `bottleneck_model.ipynb`: The main Jupyter Notebook containing the full data pipeline from EDA to model evaluation.
- `Datasets/`: Contains the `Big_data_dataset.csv` data used for training and evaluating the model.
- `docs/`: Additional documentation and presentations (e.g., `Presentation FA2 in pdf.pdf`).
- `results/`: Output directories for generated model evaluation charts and results.
- `requirements.txt`: Python dependencies required to run the notebook.

## ⚙️ Pipeline Stages

1. **Stage 1**: Data Loading & Exploratory Data Analysis (EDA)
2. **Stage 2**: Data Preprocessing (Scaling, Train/Test Split)
3. **Stage 3**: Handling Class Imbalance (SMOTE)
4. **Stage 4**: Model Training & Comparison (using XGBoost and other classifiers)
5. **Stage 5**: Model Evaluation (Metrics, Confusion Matrix, ROC Curves)
6. **Stage 6**: Bottleneck Point Prediction & Visualization

## 🛠️ Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AtharvHuilgol/System-Bottleneck_Prediction.git
   cd System-Bottleneck_Prediction
   ```

2. **Create a virtual environment (Optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Notebook:**
   Start Jupyter Notebook or open the notebook in your favorite IDE (like VS Code) to run the `bottleneck_model.ipynb` file.

## 📊 Dataset

- **Source**: `Datasets/Big_data_dataset.csv`
- **Target Variable**: `status` column 
  - `0` = Working
  - `1` = Bottleneck
- **Challenge**: Extreme class imbalance (99% Working vs 1% Bottleneck)

## 🤝 Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a Pull Request.

---
*Created by [Atharv Huilgol](https://github.com/AtharvHuilgol).*
