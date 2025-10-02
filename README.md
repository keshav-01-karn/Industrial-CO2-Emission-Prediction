# 🌏**CO₂ Emission Prediction using Machine Learning**

## Table of Contents
 - [Project Overview](#project-overview)
 - [Dataset](#dataset)
 - [Exploratory Data Analysis](#exploratory-data-analysis)
 - [Machine Learning Model](#machine-learning-model)
 - [Feature Importance](#feature-importance)
 - [Classification: Emission Bands](#classification-emission-bands)
 - [Key Results & Insights](#key-results-&-insights)
 - [Limitations](#limitations)



### Project Overview
In this project, I built a **Machine Learning model** to predict **CO₂ emissions** from industrial process parameters (synthetic plant data). The project simulates how data science can be applied in **process optimization and emission reduction strategies** for sustainable operations.

Key steps include:<br>
- **Data generation** (synthetic plant operational data in CSV format).<br>
- **Exploratory Data Analysis(EDA)** with statistical summaries and visualizations.<br>
- **Regression Modeling** using **Random Forest with hyperparameter tuning**.<br>
- **Feature Importance** (Impurity & Permutation).<br>
- **Classification** of emissions into low/medium/high bands.<br>
- **Model evaluation** (R², RMSE, confusion matrix).<br>
- **Limitations** for real-world application.<br>

### Dataset
- File: [ CO2_Distillation_Dataset](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/CO2_Distillation_Dataset.csv)<br>
- Records: 2000 samples (hourly plant data).<br>
- Features include:<br>
  - Plant ID, Fuel Type<br>
  - Ambient Temperature, Steam Pressure<br>
  - Flue Gas Flow, Fuel Consumption, Production Rate<br>
  - Scrubber presence & efficiency,energy_consumption_MW<br>
- Target: co2_net_kg_hr (Net CO₂ emissions in kg/h).

### Exploratory Data Analysis
1. **Distribution of CO₂ Emissions**<br>
The distribution shows that most emissions fall around the mean with some variance — consistent with synthetic industrial     operations.📈[CO2_Emissons_Distribution](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/histogram_co2.png)
2. **Feature Correlation Matrix**<br>
Highlights that **flue gas flow, production rate, and fuel consumption** are strongly correlated with CO₂ emissions.          📈[Correlation_Matrix](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/correlation_matrix.png)<br>
3. **Scatterplots (CO₂ vs Features**)<br>
Confirms strong positive correlations with **production rate, flue gas flow, and fuel consumption**.
<img width="500" height="500" alt="features_scatter_plot" src="https://github.com/user-attachments/assets/20040bb4-8b60-49c5-b9ab-a494e9419b89" />

### Machine Learning Model
**Regression: Random Forest Regressor**<br>
- Tuned using RandomizedSearchCV<br>
- Best Parameters: <br>
  - n_estimators=100, max_depth=20, min_samples_split=5, max_features='sqrt'<br>
- Performance:<br>
  - R² ≈ 0.89<br>
  - RMSE ≈ 64.73<br>
📈[Predicted_vs_Actual Plot](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/pred_vs_actual.png)

### Feature Importance

Impurity-based importance 📈 [impurity_plot](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/feature_importance_impurity.png)<br>
Permutation importance 📈[permutation_plot](https://github.com/keshav-01-karn/Industrial-CO2-Emission-Prediction/blob/main/feature_importance_perm.png)<br>

👉 Fuel consumption, flue gas flow, and production rate are the most significant drivers of CO₂ emissions.

### Classification: Emission Bands
- Target divided into Low / Medium / High emission categories.<br>
- Model: Random Forest Classifier (200 trees)<br>
- Accuracy: 0.85<br>
- Confusion Matrix:<br>
  <img width="400" height="400" alt="conf_matrix" src="https://github.com/user-attachments/assets/87d8dd17-1cb0-4100-aaf2-865378fcb310" /> <br>
  This shows the model can reliably categorize emission ranges.

### 📊 Key Results & Insights 
  - Regression model predicts continuous CO₂ emissions with good accuracy.
  - Classification model effectively categorizes emissions into risk bands.
  - Scrubber efficiency plays a role but is less dominant than fuel/flow/production.
  - Feature importance analysis helps identify process levers for emission control.
    
### ⚠️ Limitations
  - Synthetic Data: Not validated against real plant conditions.
  - Simplified Assumptions: Emission generation logic is linear with added noise.
  - Model Scope: Does not account for advanced process dynamics or external environmental impacts.


✨ This project demonstrates how **machine learning can be leveraged in process industries** to analyze and predict CO₂ emissions, supporting **sustainability goals**.



