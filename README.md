# 🌏**CO₂ Emission Prediction using Machine Learning**

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
- File: yokogawa_co2_synthetic.csv<br>
- Records: 2000 samples (hourly plant data).<br>
- Features include:<br>
  - Plant ID, Fuel Type<br>
  - Ambient Temperature, Steam Pressure<br>
  - Flue Gas Flow, Fuel Consumption, Production Rate<br>
  - Scrubber presence & efficiency,energy_consumption_MW<br>
- Target: co2_net_kg_hr (Net CO₂ emissions in kg/h).



