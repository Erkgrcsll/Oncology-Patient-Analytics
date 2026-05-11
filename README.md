# Chemotherapy Patient Analytics & Machine Learning

# Project Overview

This project develops a complete healthcare analytics and machine learning pipeline to analyze chemotherapy patient outcomes using clinical, demographic, treatment, and survival data.

The analysis combines:
- Exploratory Data Analysis (EDA)
- Survival Analysis
- Patient Segmentation
- Machine Learning Prediction
- Explainable AI (SHAP)

The objective is to simulate how data science and artificial intelligence can support oncology treatment optimization, risk stratification, and personalized healthcare decision-making.

This project was designed as an end-to-end healthcare analytics portfolio project that demonstrates both analytical thinking and practical machine learning implementation in the healthcare domain.

---

# Clinical Problem

Chemotherapy treatment outcomes vary significantly across patients due to:
- Cancer type
- Tumor stage
- Genetic mutation
- Patient demographics
- Treatment regimen
- Side effects and toxicity

Healthcare providers often face challenges in:
- Identifying high-risk patients early
- Predicting treatment response
- Monitoring survival outcomes
- Optimizing chemotherapy strategies
- Reducing severe treatment toxicity

This project demonstrates how machine learning and healthcare analytics can assist clinicians by identifying important predictive factors and generating explainable clinical insights.

---

# Objectives

The project aims to:

## Clinical Analytics
- Analyze patient demographics and clinical characteristics
- Evaluate treatment outcomes and survival patterns
- Understand relationships between tumor stage, metastasis, toxicity, and survival

## Machine Learning
- Predict chemotherapy treatment response
- Identify the most influential clinical variables
- Create explainable prediction models using SHAP

## Patient Segmentation
- Group patients into clinically meaningful clusters
- Detect high-risk and low-survival patient groups

## Survival Analysis
- Estimate patient survival probability over time
- Compare survival across different patient groups

---

# Dataset Description

The dataset contains approximately 50,000 chemotherapy patient records.

Each row represents one patient receiving chemotherapy treatment.

---

# Dataset Features

## 1. Patient Demographics

| Feature | Description |
|---|---|
| Patient_ID | Unique patient identifier |
| Age | Patient age |
| Sex | Male or Female |
| BMI | Body Mass Index |
| Smoking_Status | Smoking history |

---

## 2. Clinical Information

| Feature | Description |
|---|---|
| Cancer_Type | Cancer diagnosis type |
| Genetic_Mutation | Genetic mutation associated with cancer |
| Tumor_Stage | Cancer stage (I–IV) |
| Tumor_Size | Tumor size measurement |
| Metastasis_Status | Indicates whether metastasis occurred |

---

## 3. Treatment Information

| Feature | Description |
|---|---|
| Chemotherapy_Regimen | Treatment protocol used |
| Dosage (mg/m²) | Chemotherapy dosage |
| Cycles_Completed | Number of chemotherapy cycles completed |

---

## 4. Side Effects & Toxicity

| Feature | Description |
|---|---|
| Nausea_Severity | Severity score of nausea |
| Neutropenia | Indicates white blood cell suppression |

---

## 5. Clinical Outcomes

| Feature | Description |
|---|---|
| Tumor_Response | Treatment response category |
| Overall_Survival_Months | Patient survival duration |

---

# Technologies Used

## Programming Language
- Python

## Data Analysis Libraries
- Pandas
- NumPy

## Visualization Libraries
- Matplotlib
- Seaborn

## Machine Learning Libraries
- Scikit-learn
- XGBoost

## Survival Analysis
- Lifelines

## Explainable AI
- SHAP

---

# Project Workflow

# 1. Data Cleaning & Preprocessing

The first step focuses on preparing the dataset for analysis.

## Activities:
- Handling missing values
- Encoding categorical variables
- Cleaning inconsistent data
- Preparing machine learning features

## Why This Matters
Healthcare datasets often contain incomplete or inconsistent information. Proper preprocessing ensures model stability and analytical reliability.

---

# 2. Exploratory Data Analysis (EDA)

EDA was performed to understand:
- Patient distributions
- Treatment outcomes
- Survival trends
- Toxicity patterns
- Relationships between clinical variables

---

## Visualizations Included

### Tumor Response Distribution
Shows the proportion of:
- Complete response
- Partial response
- Stable disease
- Progressive disease

Purpose:
- Understand overall treatment effectiveness.

---

### Cancer Type Distribution
Analyzes patient frequency across cancer categories.

Purpose:
- Detect dataset balance and prevalence.

---

### Survival by Cancer Type
Compares survival duration across cancers.

Purpose:
- Identify cancers associated with poorer prognosis.

---

### Survival by Tumor Stage
Evaluates survival differences between stages I–IV.

Purpose:
- Measure clinical severity impact.

---

### Correlation Heatmap
Measures relationships between numerical variables.

Purpose:
- Detect potential predictive patterns.

---

# 3. Survival Analysis

Kaplan-Meier Survival Analysis was used to estimate patient survival probability over time.

## Method Used
- Kaplan-Meier Estimator

## Why It Matters
Survival analysis is widely used in:
- Oncology
- Clinical trials
- Epidemiology

It helps estimate:
- Probability of survival
- Risk progression over time

---

## Output
- Kaplan-Meier Survival Curve

The curve visualizes how survival probability changes across treatment duration.

---

# 4. Patient Segmentation

K-Means clustering was applied to group patients into segments based on clinical similarity.

## Features Used
- Age
- BMI
- Tumor Size
- Chemotherapy Dosage
- Survival Months

---

## Why Segmentation Matters

Patient segmentation can help healthcare providers:
- Identify high-risk populations
- Personalize treatment strategies
- Optimize healthcare resources
- Detect clinically similar patient groups

---

## Example Segments

Possible clusters may represent:
- High survival / low tumor burden
- High toxicity / poor prognosis
- Aggressive disease profiles

---

# 5. Machine Learning Prediction

An XGBoost classification model was developed to predict tumor response.

---

## Prediction Target

Target Variable:
- Tumor_Response

Prediction Categories:
- Complete
- Partial
- Stable
- Progressive

---

## Why XGBoost?

XGBoost is commonly used because it:
- Handles structured healthcare data effectively
- Works well with mixed feature types
- Provides strong predictive performance
- Supports feature importance analysis

---

# 6. Model Evaluation

Several evaluation metrics were used:

| Metric | Purpose |
|---|---|
| Accuracy | Overall prediction performance |
| Precision | Positive prediction quality |
| Recall | Ability to detect actual classes |
| F1-Score | Balance between precision and recall |
| Confusion Matrix | Detailed prediction breakdown |

---

# 7. Explainable AI (SHAP)

SHAP (SHapley Additive exPlanations) was used to explain model predictions.

---

## Why Explainable AI Matters

In healthcare, explainability is critical because clinicians need to understand:
- Why predictions happen
- Which features drive risk
- Whether predictions are clinically reasonable

---

## SHAP Analysis Provides

- Feature importance ranking
- Individual prediction explanation
- Global model interpretability

---

## Example Insights

SHAP may reveal that:
- Metastasis strongly reduces survival probability
- Advanced tumor stage increases progression risk
- Dosage intensity influences treatment response

---

# Key Findings

## Clinical Insights

### Tumor Stage Matters
Advanced-stage cancer patients generally show poorer survival outcomes.

---

### Metastasis Influences Prognosis
Patients with metastasis tend to have higher risk and lower survival.

---

### Treatment Toxicity Impacts Outcomes
Severe neutropenia may correlate with reduced treatment tolerance.

---

### Patient Segmentation Reveals Distinct Profiles
Different clusters exhibit unique clinical characteristics and survival patterns.

---

# Business & Healthcare Impact

This project demonstrates how healthcare analytics can support:

## Clinical Decision Support
Helping clinicians identify high-risk patients earlier.

---

## Personalized Oncology
Adjusting treatment based on patient risk profiles.

---

## Explainable Clinical AI
Improving trust and interpretability in machine learning systems.

---

## Treatment Optimization
Supporting dosage and treatment planning.

---

## Risk Stratification
Prioritizing patients requiring intensive monitoring.

---

# Project Structure

```bash
├── chemotherapy_patient_data.csv
├── chemotherapy_ml_analysis.ipynb
├── README.md
