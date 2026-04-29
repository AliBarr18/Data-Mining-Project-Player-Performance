## Deliverable 2 — Exploratory Data Analysis (EDA) & Data Preparation

### Dataset
UCI Online Shoppers Purchasing Intention Dataset
- 12,330 rows, 18 columns
- Target variable: Revenue (True = purchase made, False = no purchase)

### 1. Data Overview
- No missing values found across all columns
- Mix of numeric, categorical, and boolean features
- Class imbalance: 84.5% no purchase (10,422) vs 15.5% purchase (1,908)

### 2. Key Insights from EDA
- Dataset is imbalanced — majority of visitors do not make a purchase
- PageValues shows strong correlation with Revenue
- BounceRates and ExitRates are highly correlated with each other
- Most sessions have zero PageValues, indicating low purchase intent

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
