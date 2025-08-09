<img src="Amazon-Symbol.jpg" alt="Amazon Logo" style="float: right; width: 220px; margin-left: 10px;"/>

# 📦 Amazon Delivery Route Analysis

**Author:** Jerry Barboza  
**Date:** July 2025  
**Role:** Data Analyst Portfolio Project  



---

## Abstract

Drawing on my experience working at Amazon and my academic background in Computer Science and Applied Mathematics, this project applies data analysis and machine learning techniques to evaluate delivery route efficiency and predict delivery times. Using a publicly available dataset (`amazon_delivery.csv`) containing 43,739 delivery records, the analysis identifies key operational factors affecting delivery efficiency and develops predictive models to estimate delivery times.  

The workflow included:  
- **Data Cleaning:** Removed missing or invalid values, filtered for valid geographic ranges, standardized categorical fields, and converted time fields to appropriate formats.  
- **Exploratory Data Analysis (EDA):** Examined delivery time distributions across traffic levels, weather conditions, geographic areas, and vehicle types using boxplots, histograms, and correlation heatmaps.  
- **Geospatial Analysis:** Calculated geodesic distances between store and drop-off locations; visualized delivery points using Folium maps and heatmaps.  
- **Feature Engineering:** Derived distance-based and time-based features, normalized categories, and encoded variables for modeling.  
- **Predictive Modeling:** Compared Linear Regression, Random Forest Regressor, and XGBoost Regressor models for delivery time prediction, evaluating performance using R² score and RMSE.  
- **Key Findings:** Delivery times are most influenced by traffic conditions, weather, agent ratings, and geographic distance. Ensemble models outperformed linear models, with XGBoost achieving the highest accuracy.  

---

## Summary  
- **Dataset Size:** 43,739 records from Amazon deliveries.  
- **Primary Goal:** Identify factors affecting delivery time and create predictive models.  
- **Top Predictors:**  
  - **Traffic Level:** Low traffic significantly reduces delivery time; heavy traffic (Jam) causes the longest delays.  
  - **Weather:** Sunny conditions improve delivery times; adverse weather like fog or storms increases delays.  
  - **Agent Rating:** Higher ratings correlate with faster deliveries.  
  - **Geodesic Distance:** Longer distances lead to proportionally longer delivery times.  
- **Model Performance:**  
  - Linear Regression: R² = 0.33, RMSE ≈ 41.93 min  
  - Random Forest: R² = 0.38, RMSE ≈ 40.28 min  
  - XGBoost: **R² = 0.45**, RMSE ≈ 38.11 min (best performance)  
- **Operational Insights:**  
  - Optimizing routes to avoid heavy traffic zones can yield substantial time savings.  
  - Agent training and performance management can improve delivery speed.  
  - Weather forecasting integration may help proactively adjust delivery schedules.  


## 🛠 Tools & Data

- **Notebook Environment:** Jupyter Notebooks  
- **Programming Language:** Python  
- **Libraries:** pandas, matplotlib, seaborn, geopandas, folium  
- **Dataset:** `amazon_delivery.csv` (sourced from [Kaggle](https://www.kaggle.com/))  
