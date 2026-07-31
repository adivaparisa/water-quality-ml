# 🌊 Water Quality pH Prediction

An interactive dashboard for predicting pH levels in Georgia water systems using machine learning. This project explores the relationship between water quality indicators and pH, providing insights for water quality monitoring.

**🔗 Live Demo:** [https://adivaparisa.github.io/water-quality-ml/](https://adivaparisa.github.io/water-quality-ml/)

---

## 📊 Project Overview

This project analyzes water quality data from 37 monitoring locations across Georgia to predict median pH levels. By leveraging water quality indicators like dissolved oxygen, conductance, and temperature, we demonstrate that pH can be accurately predicted using machine learning models.

### Key Highlights
- **🎯 Best Model:** Gradient Boosting (**R² = 0.84**, RMSE = 0.0128)
- **🔑 Top Predictor:** Maximum Dissolved Oxygen (**r = 0.877**)
- **📈 Dataset:** 15,651 records across 423 days
- **📍 Locations:** 37 monitoring sites

---

## 📁 Dataset

The dataset contains daily water quality measurements from the Georgia water system. Features include:

| Feature | Description |
|---------|-------------|
| **Conductance** | Maximum, minimum, and mean specific conductance |
| **Dissolved Oxygen** | Maximum, minimum, and mean dissolved oxygen |
| **Temperature** | Maximum, minimum, and mean water temperature |
| **pH (Target)** | Median pH (normalized to 0–1 scale) |

> **Note:** pH maximum and minimum were excluded from modeling to prevent information leakage.

---

## 🧪 Methodology

### 1. Exploratory Data Analysis (EDA)
- **pH Distribution:** The target variable is normally distributed with values between 0.57–0.96.
- **Correlation Analysis:** Maximum dissolved oxygen shows the strongest correlation with pH (`r = 0.877`), while temperature shows minimal linear relationship.

### 2. Modeling
Three models were evaluated using a time-based train-test split:
- **Linear Regression:** R² = 0.832
- **Random Forest:** R² = 0.788
- **Gradient Boosting:** **R² = 0.842** (Best Performing)
  
## 🤖 Model Performance Comparison

| Model | R² | RMSE | MAE |
|-------|----|------|-----|
| **Gradient Boosting** | **0.842** | **0.0128** | **0.0082** |
| Linear Regression | 0.832 | 0.0132 | 0.0083 |
| Random Forest | 0.788 | 0.0148 | 0.0085 |
| Mean Baseline | -0.077 | 0.0334 | 0.0246 |

### 3. Feature Importance
The Gradient Boosting model identified **maximum dissolved oxygen** as the most influential feature by a significant margin.

## 💡 Key Insights

- **Dissolved oxygen (maximum)** is the strongest predictor of pH (`r = 0.877`).
- **Gradient Boosting** achieved the best performance with **R² = 0.842**.
- **Conductance** shows moderate correlation with pH.
- **Temperature** has minimal linear relationship with pH.

### Implications
These findings suggest that **dissolved oxygen** and **conductance measurements** are key indicators for monitoring water quality and predicting pH levels in Georgia water systems.

## 👤 Author

**Adiva Parisa and Monisha Majumder**

