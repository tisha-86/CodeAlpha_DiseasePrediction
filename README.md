# CodeAlpha_DiseasePrediction

## 📌 Objective
Predict whether a patient has heart disease based on clinical parameters (age, blood pressure, cholesterol, etc.) using classification algorithms. This project is submitted as **Task 4: Disease Prediction from Medical Data** for the CodeAlpha Machine Learning Internship.

## 📊 Dataset
- **Source:** UCI Machine Learning Repository — Heart Disease (Cleveland) Dataset
- **Size:** 303 patient records, 14 attributes
- **Target variable:** `target` (1 = heart disease present, 0 = no heart disease)

**Features used:**
`age`, `sex`, `cp` (chest pain type), `trestbps` (resting blood pressure), `chol` (cholesterol), `fbs` (fasting blood sugar), `restecg` (resting ECG results), `thalach` (max heart rate achieved), `exang` (exercise-induced angina), `oldpeak` (ST depression), `slope`, `ca` (major vessels colored by fluoroscopy), `thal`

## ⚙️ Approach
1. **Data Loading & Cleaning** — checked for missing values, verified class balance.
2. **Exploratory Data Analysis** — correlation heatmap, target distribution plot.
3. **Preprocessing** — train/test split (80/20, stratified), feature scaling with `StandardScaler`.
4. **Model Training** — compared three classification algorithms:
   - Logistic Regression
   - Random Forest
   - Support Vector Machine (RBF kernel)
5. **Evaluation** — Accuracy, Precision, Recall, F1-Score, ROC-AUC for each model.
6. **Visualization** — ROC curves, confusion matrix, and feature importance (Random Forest).

## 🏆 Results

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---------------------|----------|-----------|--------|----------|---------|
| Random Forest        | 0.82     | 0.76      | 0.97   | 0.85     | **0.91**|
| SVM (RBF kernel)     | 0.82     | 0.78      | 0.94   | 0.85     | 0.88    |
| Logistic Regression  | 0.80     | 0.77      | 0.91   | 0.83     | 0.87    |

**Best model: Random Forest**, with the strongest ROC-AUC (0.91) and highest recall (0.97) — important in a medical context where missing an actual disease case is costlier than a false alarm.

The most predictive features (from Random Forest feature importance) were **thal (thalassemia)**, **cp (chest pain type)**, and **ca (major vessels colored by fluoroscopy)**.

## 📁 Files in this repo
- `heart-disease-data-2026.ipynb` — full training & evaluation notebook
- `heart.csv` — dataset used
- `model_comparison.csv` — metrics table for all models
- `correlation_heatmap.png` — feature correlation heatmap
- `target_distribution.png` — class balance plot
- `roc_curves.png` — ROC curve comparison across models
- `confusion_matrix_best_model.png` — confusion matrix for the best model
- `feature_importance.png` — Random Forest feature importance

## 🔧 Tools & Libraries
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## 🎓 Internship
This project was completed as part of the **CodeAlpha Machine Learning Internship**.
🔗 [www.codealpha.tech](https://www.codealpha.tech)
