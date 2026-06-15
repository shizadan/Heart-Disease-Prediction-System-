# 🫀 Heart Disease Risk Predictor

A machine learning web app that predicts a patient's risk of heart disease based on clinical attributes, built and deployed with Streamlit.

🔗 **Live App:** https://ntwthqycqubaejjkod7b9l.streamlit.app/

## Overview
This project uses a dataset of 1,025 patient records with 13 clinical features (age, blood pressure, cholesterol, max heart rate, ECG results, etc.) to predict the presence of heart disease. Built as part of my AI & Data Science Bootcamp — Week 3 assignment.

## Dataset
- **Source:** UCI Heart Disease Dataset
- **1,025 rows, 13 features, 1 target**
- Target: `1` = heart disease present, `0` = no heart disease
- No missing values

## Features Used
| Feature | Description |
|---|---|
| age | Age in years |
| sex | 1 = Male, 0 = Female |
| cp | Chest pain type (0–3) |
| trestbps | Resting blood pressure (mm Hg) |
| chol | Serum cholesterol (mg/dl) |
| fbs | Fasting blood sugar > 120 mg/dl |
| restecg | Resting ECG results (0–2) |
| thalach | Maximum heart rate achieved |
| exang | Exercise-induced angina |
| oldpeak | ST depression induced by exercise |
| slope | Slope of peak exercise ST segment |
| ca | Number of major vessels (0–3) |
| thal | Thalassemia type (0–3) |

## Approach
1. Exploratory Data Analysis (distributions, correlations, class balance)
2. Preprocessing: feature scaling with `StandardScaler`
3. Train/test split: 80/20 with stratification
4. Models trained: Logistic Regression & Random Forest
5. Evaluation: Accuracy, ROC-AUC, Confusion Matrix, Classification Report

## Results
| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | 0.8098 | 0.9298 |
| Random Forest | 1.0000 | 1.0000 |

> **Note:** The Random Forest's perfect score (1.0) likely indicates overfitting or data leakage (this dataset is known to contain duplicate/near-duplicate rows). The Logistic Regression result (81% accuracy, 0.93 AUC) is a more realistic estimate of real-world performance.

## Tech Stack
- Python, pandas, scikit-learn, matplotlib, seaborn
- Streamlit (deployment)
- joblib (model persistence)
- Google Colab (development environment)

## Repository Contents
| File | Description |
|---|---|
| `notebook.ipynb` | Full Jupyter notebook with EDA, model training & evaluation |
| `app.py` | Streamlit web application |
| `requirements.txt` | Python dependencies |
| `heart_gtigwd.csv` | Dataset |
| `heart_disease_model.pkl` | Saved Random Forest model |
| `scaler.pkl` | Saved StandardScaler |

## How to Run Locally
```bash
pip install -r requirements.txt
streamlit run app.py
```

## Disclaimer
This tool is for educational purposes only and does not constitute medical advice. Always consult a qualified healthcare professional.

## Author
**Dan Shina** — Senior Manager transitioning into AI & Data Science
- GitHub: [shizadan](https://github.com/shizadan)
- LinkedIn: [(https://www.linkedin.com/in/dan-s-85a502ba/)]
