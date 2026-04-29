# Online Shoppers Purchasing Intention — Predictive Modeling Project

## Project Overview
This project predicts whether an online shopper will make a purchase based on 
their browsing behavior and session characteristics using machine learning classification models.

---

## Deliverable 1 — Problem Definition & Data Acquisition

### 1. Problem Statement
The goal of this project is to predict whether an online visitor will generate 
revenue (make a purchase) based on their browsing behavior, session characteristics, 
and engagement patterns.

### 2. Target Variable
- **Variable:** Revenue
- **Type:** Binary (True = purchase made, False = no purchase)

### 3. Use Case / Domain Context
This project is in the e-commerce and digital marketing domain. Predicting purchase 
likelihood helps businesses:
- Identify high-value visitors in real time
- Personalize recommendations and promotions
- Reduce wasted ad spend
- Increase overall conversion rates

### 4. Dataset
- **Source:** UCI Machine Learning Repository — Online Shoppers Purchasing Intention Dataset
- **Size:** 12,330 sessions, 18 features
- **Features:** Page visits, bounce rates, exit rates, visitor type, traffic type, and more

### 5. Potential Value
A successful model can provide:
- Real-time conversion prediction
- Improved ad targeting
- Better customer segmentation
- Optimized website experience

---

## Deliverable 2 — Exploratory Data Analysis (EDA) & Data Preparation

### 1. Data Overview
- 12,330 rows, 18 columns
- No missing values found
- Mix of numeric, categorical, and boolean features
- Class imbalance: 84.5% no purchase (10,422) vs 15.5% purchase (1,908)

### 2. Key Insights from EDA
- PageValues shows the strongest correlation with Revenue
- BounceRates and ExitRates are highly correlated with each other
- Most sessions have zero PageValues, indicating low purchase intent
- Dataset is imbalanced — majority of visitors do not make a purchase

### 3. Data Preparation
- Encoded categorical variables (Month, VisitorType) using Label Encoding
- Converted boolean columns (Weekend, Revenue) to integers
- Split data: 80% training, 20% testing with stratification

### 4. Visualizations
- Class balance bar chart
- Correlation heatmap
- PageValues distribution histogram
- Bounce Rate vs Exit Rate scatterplot

### 5. Notebook
See deliverable2_eda.ipynb for full code and visualizations

## Deliverable 3 — Modeling, Evaluation & Insights

### Models Trained
| Model | Accuracy | Precision | Recall | F1 | Kappa |
|---|---|---|---|---|---|
| Random Forest | 0.8998 | 0.7320 | 0.5576 | 0.6330 | 0.5762 |
| Logistic Regression | 0.8820 | 0.7514 | 0.3560 | 0.4831 | 0.4259 |
| Tuned Random Forest | 0.9015 | 0.7405 | 0.5602 | 0.6379 | 0.5821 |

### Best Model
Tuned Random Forest — highest accuracy (90.15%) and best overall balance of metrics

### Top 5 Features
1. PageValues (0.3859)
2. ExitRates (0.0901)
3. ProductRelated_Duration (0.0868)
4. ProductRelated (0.0726)
5. Administrative_Duration (0.0596)

### Actionable Insights
- PageValues is the strongest predictor of purchase intent
- High exit rates signal low purchase intent — target these users with promotions
- Shoppers who spend more time on product pages are more likely to convert
- Dataset is imbalanced — future work could use SMOTE to improve recall

### Notebook
See deliverable2_eda.ipynb for full code, visualizations, and model results
