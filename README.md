# Developer Income Prediction & Clustering (CRISP-DM)

This repository contains the machine learning coursework completed as part of the **“Machine Learning and AI for Data Analysis”** module at Nottingham Trent University. The project applies the **CRISP-DM methodology** to the 2021 freeCodeCamp New Coder Survey dataset, focusing on:

- Predicting whether a developer falls into the **high-income** or **low-income** category  
- Identifying natural subgroups using **K-Means clustering**
- Performing detailed **data cleaning, EDA, modelling, tuning, and evaluation**

> 📄 Full coursework report with figures, EDA visuals, cluster analysis, model evaluation, and ROC curves:  
> `docs/ML_Coursework_Report.pdf`

---

## 📌 Project Overview

This project follows the **CRISP-DM framework**, running through all six phases:

### **1. Business Understanding**
Understanding factors influencing income levels of new programmers—experience, education, learning habits, age, etc.

### **2. Data Understanding**
Dataset attributes include:  
WeeklyHoursSpent, MonthsProgExp, EduLevel, EmploymentStatus, AnnualIncomeUSD, Age, InterestInDevCareer, Region.

The PDF (pages 4–7) provides full justification for each attribute and their relevance in income prediction. :contentReference[oaicite:3]{index=3}

### **3. Data Preparation**
Steps included:
- Removing unrealistic values (e.g., >100 weekly hours)
- Cleaning age to keep 16–80  
- Handling missing values (median imputations, categorical encodings)
- Transforming AnnualIncomeUSD into **ordinal numeric levels**
- Encoding categorical variables for ML

The notebook contains all preprocessing code.

### **4. Modelling**
Models trained:

- k-Nearest Neighbours  
- Random Forest  
- Gradient Boosting Machines / XGBoost  
- Neural Network  
- Ensembles (RFC+SVM, RFC+GBM Soft Voting)

Hyperparameter tuning performed using Grid Search / Randomized Search.

### **5. Evaluation**
Metrics include:
- Accuracy  
- Confusion Matrices  
- ROC Curves & AUC Values

Top scores from the report (page 31):  
- Neural Network → **81%**  
- GBM → **80.39%**  
- RFC → **79.39%**  
- k-NN → **78.22%**

All confusion matrices & ROC curves are included in the PDF (pages 27–31). :contentReference[oaicite:4]{index=4}

### **6. Deployment (theoretical)**
Discusses how such models could be applied in real-world scenarios, e.g.:
- recruiting strategies  
- coding bootcamp targeting  
- developer segmentation  

---

## 📊 Clustering Analysis

Clustering was performed separately on:
- **High-income group**  
- **Low-income group**

Using **K-Means (k=3)** selected via elbow method.

Findings include:
- Clusters of novices, intermediates, and experienced coders  
- Variations in coding hours, education, and age  
- Multiple pathways into tech across age groups  
