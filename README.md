# Midterm Project: Heart Disease Classification Analysis
**Author:** Kellie Leopold  
**Date:** November 11, 2025  
**Objective:** Predict the risk of heart disease using patient data.

---

## Introduction

Heart disease is a leading cause of death worldwide. Early detection helps healthcare providers take preventive measures. This project uses the UCI Heart Disease dataset to analyze patient data and build machine learning models to predict heart disease risk.

**Project Goals:**

- Explore and understand the dataset  
- Preprocess and engineer meaningful features  
- Train and evaluate classifiers for heart disease prediction  
- Compare models and interpret results  

---

## Dataset

- **Records:** 303  
- **Features:** 14 (age, sex, chest pain type, blood pressure, cholesterol, etc.)  
- **Target:** Binary (`0 = no significant heart disease`, `1 = heart disease present`)  

**Observations:**

- A few missing values: `ca` (4), `thal` (2) – filled with medians  
- Target simplified from multi-class (0–4) to binary  
- Mix of numeric and categorical features  

---

## Features & Preprocessing

**Features used:**

1. **Age Group:** young (<40), middle (40–60), senior (>60)  
2. **Blood Pressure Level:** normal, elevated, high  
3. **Cholesterol:** numeric values  

**Engineering Steps:**

- Binned age and blood pressure to capture non-linear risk patterns  
- Mapped sex to categorical labels (male/female)  
- Ensured all features are numeric for modeling compatibility  

---

## Models

**Classifiers Tested:**

| Model | Purpose |
|-------|---------|
| Decision Tree | Interpretable, handles thresholds well |
| SVC | Handles non-linear boundaries |
| Neural Network | Captures complex relationships |

**Training:** 80/20 train-test split, evaluated on each feature individually  

---

## Results

**Decision Tree Accuracy (single features):**

| Feature | Accuracy |
|---------|----------|
| Age Group | 0.59 |
| Blood Pressure | 0.59 |
| Cholesterol | 0.64 |

**Insights:**

- Cholesterol is the strongest single predictor, followed by blood pressure  
- Age alone is weaker but still provides context  
- Decision Trees generally performed better or as well as other models for single features  
- Combining multiple features would likely improve performance  

**Reflection:**

- Age alone is a general indicator, so predictions were weaker  
- Blood pressure improved predictive power slightly  
- Cholesterol gave the clearest results, aligning with medical knowledge  
- Using multiple features together would likely give the best predictions  

---

## Challenges

- Converting multi-class target to a meaningful binary outcome  
- Handling missing values and numeric conversions for `ca` and `thal`  
- Low predictive power for single features, especially age  
- Neural Network struggled with class imbalance in cholesterol predictions  

---

## Possible Next Steps

- Build a model combining multiple features (age, blood pressure, cholesterol, etc.)  
- Use cross-validation for more robust evaluation  
- Explore hyperparameter tuning and feature selection  

---

## Key Learnings

- Combining multiple features improves prediction accuracy  
- Preprocessing and feature engineering are critical for model performance  
- Medical context helps select meaningful predictors  
- Different models have varying strengths depending on feature type and dataset size  
- Exploratory data analysis and model comparison are essential steps in building predictive models  