# Diabetes Prediction Model

A comprehensive machine learning project for predicting diabetes using multiple classification algorithms and advanced data preprocessing techniques.

## Project Overview

This project implements and compares three machine learning models to predict diabetes based on patient health metrics:
- **Logistic Regression**
- **Random Forest (with Hyperparameter Tuning)**
- **Gradient Boosting**

## Features

✨ **Data Processing**
- Missing value imputation using median strategy
- Feature scaling using StandardScaler
- Stratified train-test split for balanced datasets

✨ **Model Development**
- Multiple classification algorithms
- Grid Search for hyperparameter optimization
- Cross-validation (5-Fold CV)
- Comprehensive evaluation metrics

✨ **Evaluation Metrics**
- Accuracy Score
- AUC-ROC Score
- F1-Score
- Precision & Recall
- Confusion Matrix
- Classification Report

✨ **Visualizations**
- Correlation Heatmaps
- Distribution Plots
- ROC Curves Comparison
- Confusion Matrices
- Feature Importance Plots
- Model Performance Comparison

## Dataset

**File:** `diabetes.csv`

**Features:** 8 input features
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

**Target:** Outcome (0 = No Diabetes, 1 = Diabetes)

## Model Performance

| Model | Accuracy | AUC-ROC | F1-Score |
|-------|----------|---------|----------|
| Logistic Regression | 70.78% | 0.8130 | 0.5455 |
| Random Forest (Tuned) | **74.68%** | 0.8144 | 0.6061 |
| Gradient Boosting | 74.68% | **0.8150** | **0.6214** |

**Best Model:** Gradient Boosting (highest AUC-ROC and F1-Score)

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/ajaysai157/diabetes-prediction
   cd diabetes-prediction
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running the Notebook

1. **Start Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

2. **Open `diabetes_pred_project.ipynb`**
   - The notebook contains all data preprocessing, model training, and evaluation steps
   - Run cells sequentially to reproduce results
   - Ensure `diabetes.csv` is in the same directory

### Running Individual Sections

The notebook is organized into clear sections:
- Data Loading & Preprocessing
- Exploratory Data Analysis
- Feature Engineering & Scaling
- Model Training & Evaluation
- Cross-Validation
- Visualizations

## File Structure

```
diabetes-prediction/
├── diabetes_pred_project.ipynb    # Main notebook with full pipeline
├── diabetes.csv                   # Dataset (768 samples)
├── requirements.txt               # Python dependencies
├── .gitignore                     # Git ignore file
└── README.md                      # This file
```

## Key Findings

### Feature Importance (from Random Forest)
1. **Glucose** - Most important (0.30)
2. **BMI** - Second most important (0.17)
3. **Age** - Third (0.13)
4. **DiabetesPedigreeFunction** - Fourth (0.12)
5. **Insulin** - Fifth (0.10)

### Model Insights
- **Gradient Boosting** achieves the best AUC-ROC (0.8150), indicating superior ranking of predictions
- **Random Forest** provides excellent feature importance insights
- Feature scaling significantly improves Logistic Regression performance
- Class imbalance exists (65.1% negative, 34.9% positive cases) - stratified split helps address this

## Technologies Used

- **Python 3.12+**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **scikit-learn** - Machine learning algorithms
- **matplotlib & seaborn** - Data visualization
- **Jupyter** - Interactive notebooks

## Results & Interpretation

### Confusion Matrix Interpretation
- **True Positives (TP):** Correctly identified diabetes cases
- **True Negatives (TN):** Correctly identified non-diabetic cases
- **False Positives (FP):** Incorrectly flagged as diabetic (Type I error)
- **False Negatives (FN):** Missed diabetes cases (Type II error) - more critical

### Model Selection
- Use **Gradient Boosting** for production when ranking predictions is important
- Use **Random Forest** for interpretability and feature importance analysis
- Use **Logistic Regression** for fast inference and explainability

## Future Improvements

- [ ] Feature engineering (polynomial features, interactions)
- [ ] Address class imbalance (SMOTE, class weights)
- [ ] Ensemble methods (Voting, Stacking)
- [ ] Deep learning models
- [ ] Hyperparameter tuning for Gradient Boosting
- [ ] Feature selection techniques (mutual information, permutation importance)
- [ ] Model deployment (Flask/FastAPI)
- [ ] Cross-validation with different folds

## Contributors

- Ajay Sai

## License

This project is open source and available under the MIT License.

## References

- UCI Machine Learning Repository - Diabetes Dataset
- scikit-learn Documentation
- Machine Learning Best Practices

---

**Last Updated:** March 9, 2026
