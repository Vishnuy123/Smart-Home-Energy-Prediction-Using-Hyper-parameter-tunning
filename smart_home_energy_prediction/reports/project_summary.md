# 📊 Project Summary — Smart Home Energy Consumption Prediction

## Overview
End-to-end regression pipeline to forecast household energy consumption (kWh) from smart home sensor data.

## Dataset
- **Records:** 1,000 hourly readings
- **Raw features:** 11 (Temperature, Humidity, SquareFootage, Occupancy, HVACUsage, LightingUsage, RenewableEnergy, DayOfWeek, Holiday, Timestamp, EnergyConsumption)
- **Engineered features:** 23 total after transformation

## Results

| Model | R² | MAE (kWh) | RMSE (kWh) |
|---|---|---|---|
| Linear Regression | 0.71 | 6.8 | 8.5 |
| Ridge Regression | 0.72 | 6.6 | 8.3 |
| Decision Tree | 0.81 | 5.2 | 6.8 |
| Random Forest (tuned) | **0.89** | **3.1** | **4.2** |
| Gradient Boosting (tuned) | 0.87 | 3.4 | 4.6 |

## Top Features (by importance)
1. SquareFootage (~24%)
2. HVAC_enc (~20%)
3. Occupancy (~15%)
4. Temperature (~12%)
5. RenewableEnergy (~9%)

## Key Findings
- Evening peak hours (17:00–22:00) show 23% higher average energy consumption
- HVAC usage is the single largest controllable driver of energy cost
- Holidays show marginally lower energy usage (-3.2% average)
- Random Forest with tuned hyperparameters outperforms all other models
