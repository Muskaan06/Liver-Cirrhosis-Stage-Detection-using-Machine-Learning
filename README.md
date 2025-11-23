# Liver Cirrhosis Stage Detection using Machine Learning

This project builds a machine learning model to predict the **histologic stage of liver cirrhosis** using patient-level clinical variables.  
It uses real clinical data from a **Mayo Clinic study** on primary biliary cirrhosis (PBC) conducted between 1974–1984.

Unlike simple binary classification medical models, this project deals with **multi-class disease staging**, making it a more medically advanced and complex prediction task.

---

## Problem Overview

The dataset contains multiple clinical, biochemical, and diagnostic features.  
The target variable is **Stage** ∈ {1, 2, 3}, representing increasing severity of liver cirrhosis.

### **Dataset Features**

| Feature | Description |
|--------|-------------|
| N_Days | Days until death, transplant, or study end |
| Status | C: censored, CL: censored (liver transplant), D: death |
| Drug | D-penicillamine or placebo |
| Age | Age in days |
| Sex | M/F |
| Ascites | Y/N |
| Hepatomegaly | Y/N |
| Spiders | Y/N |
| Edema | N, S, or Y |
| Bilirubin | Serum bilirubin |
| Cholesterol | Serum cholesterol |
| Albumin | Albumin level |
| Copper | Urine copper |
| Alk_Phos | Alkaline phosphatase |
| SGOT | SGOT enzyme level |
| Tryglicerides | Triglycerides |
| Platelets | Platelet count |
| Prothrombin | Prothrombin time |
| **Stage** | Target class: 1, 2, or 3 |

---

## Methodology

### **1. Exploratory Data Analysis**
- Feature uniqueness and distribution  
- Detecting missing values  
- Understanding categorical/ordinal variables  
- Identifying class imbalance  

### **2. Data Preprocessing**
- Label encoding for categorical features  
- Standard scaling for numerical variables  
- Handling missing values  
- Splitting dataset into training & testing sets  

### **3. Model Training**
- Baseline model comparisons  
- Hyperparameter tuning (RandomizedSearchCV)  
- Final model: **LightGBM (LGBMClassifier)**  

### **4. Why LightGBM?**
- Handles mixed feature types  
- Handles nonlinearity extremely well  
- Fast and scalable  
- Best empirical performance in this project  

---

## 📊 Final Model Performance

The notebook produced the following evaluation results:

---

### **Classification Report**

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| **1** | 0.97 | 0.95 | 0.96 | 1657 |
| **2** | 0.95 | 0.97 | 0.96 | 1697 |
| **3** | 0.98 | 0.98 | 0.98 | 1646 |
| **Accuracy** |  |  | **0.97** | 5000 |
| **Macro Avg** | 0.97 | 0.97 | 0.97 | 5000 |
| **Weighted Avg** | 0.97 | 0.97 | 0.97 | 5000 |

Test accuracy: 96.78%




