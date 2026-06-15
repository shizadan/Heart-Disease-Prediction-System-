# 🚗 Car Price Prediction — End-to-End Machine Learning Project

**Bootcamp Assignment 2 | Linear Regression**  
**Author:** Dan Shizamuayi Shina

---

## Project Overview

This project builds a machine learning model that predicts the **selling price of used cars** based on their features. It was developed as a complete end-to-end regression project covering data exploration, preprocessing, model training, evaluation, and business insights.

The dataset contains **301 records** of used cars with features such as fuel type, transmission, kilometres driven, age, and present showroom price.

---

## Dataset

| Column | Description |
|---|---|
| Car_Name | Model name |
| Year | Year of manufacture |
| Selling_Price | **Target** — price sold (₹ Lakhs) |
| Present_Price | Current ex-showroom price (₹ Lakhs) |
| Kms_Driven | Total kilometres driven |
| Fuel_Type | Petrol / Diesel / CNG |
| Seller_Type | Dealer or Individual |
| Transmission | Manual or Automatic |
| Owner | Number of previous owners |

---

## Steps Taken

1. **Problem Understanding** — Defined the business goal and identified features vs target variable
2. **EDA** — Checked missing values, summary statistics, visualised distributions and relationships
3. **Preprocessing** — Dropped high-cardinality column (Car_Name), engineered `Car_Age` from `Year`, label-encoded categorical variables
4. **Model Building** — Trained a Linear Regression model on an 80/20 train-test split
5. **Evaluation** — Assessed with MAE, RMSE, and R² Score; plotted Actual vs Predicted and Residuals
6. **Predictions** — Generated predictions for 5 sample cars
7. **Insights** — Interpreted feature coefficients and surfaced surprising findings from the data

---

## Repository Structure

```
car-price-prediction/
├── Car_Price_Prediction.ipynb   # Main notebook
├── car_data_cleaned.csv         # Preprocessed dataset
└── README.md                    # This file
```

---

## How to Run the Notebook

### Option 1 — Google Colab (Recommended)

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Upload notebook** and select `Car_Price_Prediction.ipynb`
3. Run **Cell 1** to install/import all libraries
4. When you reach the **data loading cell**, upload `Car_data.csv` when prompted
5. Run all remaining cells in order (`Runtime → Run all`)

### Option 2 — Local (Jupyter)

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch notebook
jupyter notebook Car_Price_Prediction.ipynb
```

---

## Key Results

| Metric | Score |
|---|---|
| MAE | ~1.8 Lakhs ₹ |
| RMSE | ~3.2 Lakhs ₹ |
| R² Score | ~0.84 |

The model explains approximately **84% of variance** in used car prices.

---

## Top Insights

- **Present Price** is the strongest predictor of resale value
- **Car Age** significantly reduces selling price — older cars sell for less
- **Diesel & Automatic** cars command a price premium
- **High mileage** lowers price but has less impact than age
