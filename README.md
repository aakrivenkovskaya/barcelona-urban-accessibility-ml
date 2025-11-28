# 🏙️ Barcelona Accessibility Intelligence System  
### Applied Machine Learning for Urban Policy, Inclusive Mobility & City-Level Decision Support

This repository presents an end-to-end **urban accessibility intelligence system**, designed using applied machine learning and geospatial analytics.  
The solution transforms raw municipal data into actionable insights, supporting **data-driven decisions for city planning, mobility design and inclusive public-space strategy**.

---

## 📘 Project Overview

Modern cities require infrastructure that is safe, accessible and equitable for all citizens.  
Using high-resolution open geospatial data from **Open Data BCN**, this project builds a **production-oriented ML pipeline** that predicts accessibility levels across Barcelona’s street network.

The system is designed to:
- identify accessibility gaps  
- support resource prioritization  
- guide planners in building inclusive, navigable environments  

---

## 📊 Dataset

- **Source:** Open Data BCN — `2022_Accesibilitat_barris.csv`  
- **Records:** 173,144  
- **Features:** 40 attributes describing physical street characteristics  
- **Target:** Binary indicator of street accessibility  

The dataset reflects the complexity of Barcelona’s urban fabric, enabling high-quality model learning.

---

## 🧬 ML Pipeline

### 1. **Data Loading & Initial Exploration**
- Inspection of dataset integrity  
- Target imbalance quantification  
- Validation of datatypes and structures  

---

### 2. **Preprocessing**
- Missing-value handling  
- Outlier detection using IQR/z-score  
- Datatype corrections across all 40 features  
- Distribution analysis to monitor stability  

---

### 3. **Data Preparation**
- One-hot encoding for categorical variables  
- Numerical feature scaling  
- **SMOTE oversampling** to correct imbalance  
- Stratified train/test split  

---

### 4. **Exploratory Data Analysis (EDA)**
- Correlation analysis  
- Distribution differences between accessible vs non-accessible areas  
- Feature behavior across districts  

---

### 5. **Feature Selection**
- Feature importance from tree-based models  
- Dimensionality reduction  
- Selection of high-impact, policy-relevant predictors  

---

### 6. **Modelling**
Evaluated models:
- Logistic Regression  
- Gradient Boosting  
- Random Forest  

A unified hyperparameter-tuning workflow using **RandomizedSearchCV** identifies the strongest model.

**Final chosen model:** **Random Forest** (best balance of stability and performance).

---

### 7. **Model Evaluation**
Metrics:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  

The model demonstrates strong performance across both classes.

---

### 8. **Final Validation**
- **k-fold cross-validation** for generalisation  
- Average CV accuracy: **99.6%**

---

### 9. **Model Export**
The final Random Forest model is exported using `joblib`, enabling integration into:
- GIS platforms  
- urban dashboards  
- municipal planning tools  

---

### 10. **Sample Input File**
A `sample.csv` file is included as an example schema for predictions.

---

### 11. **Geospatial Visualisation**
Interactive maps highlight:
- 🟢 Accessible areas  
- 🔴 Non-accessible areas  

Supporting data-driven prioritisation and mobility planning.

---

## 🌍 Social Impact

Improving urban accessibility has a direct influence on social inclusion, mobility equity and quality of life for people with disabilities, elderly citizens and families with limited mobility.  
This system helps identify structural barriers in the city’s infrastructure, supporting:

- evidence-based municipal planning  
- fair allocation of public resources  
- data-driven prioritisation of interventions  
- creation of safer, more inclusive neighborhoods  

By translating raw accessibility data into actionable insights, the project contributes to a more equitable and human-centered urban environment.

---

## 🔍 Key Highlights

- Production-style ML workflow designed for urban analytics  
- Robust handling of class imbalance (SMOTE)  
- High-performing Random Forest model  
- 99.6% cross-validated accuracy  
- Geospatial visualisations for decision support  
- Reproducible, clean and extendable applied ML pipeline  
