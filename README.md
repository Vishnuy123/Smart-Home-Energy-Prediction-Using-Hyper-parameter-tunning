# 🏠 Smart Home Energy Consumption Prediction

> **Machine Learning project to forecast household energy consumption using environmental and occupancy features.**

---

## 📌 Project Overview

This project builds and compares multiple machine learning models to predict smart home energy consumption (kWh) from sensor data including temperature, humidity, square footage, occupancy, HVAC/lighting usage, and renewable energy availability.

The best ensemble model achieved an **R² score of 0.89+** with an **18% improvement** over the baseline through systematic hyperparameter tuning and feature engineering.

---

## 🗂️ Project Structure

```
smart_home_energy_prediction/
│
├── data/
│   └── Energy_consumption.csv          # Raw dataset (1,000 hourly records)
│
├── notebooks/
│   ├── 01_EDA.ipynb                    # Exploratory Data Analysis
│   ├── 02_Data_Cleaning_Transformation.ipynb  # Preprocessing & feature engineering
│   ├── 03_Model_Training_Evaluation.ipynb     # Model training, tuning & comparison
│
├── models/
│   └── best_model.pkl                  # Saved best model (Random Forest)
│
├── outputs/
│   ├── eda_plots/                      # EDA visualizations
│   ├── model_comparison.png            # Model performance comparison chart
│   └── feature_importance.png         # Feature importance plot
│
├── reports/
│   └── project_summary.md             # Project findings summary
│
├── requirements.txt                    # Python dependencies
└── README.md                           # This file
```

---

## 📊 Dataset

| Feature | Type | Description |
|---|---|---|
| Timestamp | DateTime | Hourly readings (2022) |
| Temperature | Float | Ambient temperature (°C) |
| Humidity | Float | Relative humidity (%) |
| SquareFootage | Float | Home size (sq ft) |
| Occupancy | Int | Number of occupants |
| HVACUsage | Binary | HVAC system on/off |
| LightingUsage | Binary | Lighting system on/off |
| RenewableEnergy | Float | Renewable energy available (kWh) |
| DayOfWeek | Categorical | Day of week |
| Holiday | Binary | Holiday yes/no |
| **EnergyConsumption** | **Float** | **Target variable (kWh)** |

**Dataset size:** 1,000 hourly records · 11 features · No missing values

---

## 🧠 Models Trained

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression (baseline) | ~6.8 | ~8.5 | ~0.71 |
| Decision Tree | ~5.2 | ~6.8 | ~0.81 |
| Random Forest (tuned) | ~3.1 | ~4.2 | ~0.89 |
| Gradient Boosting | ~3.4 | ~4.6 | ~0.87 |

**Best model:** Random Forest (n_estimators=200, max_depth=15)

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/vishnuraj333/smart-home-energy-prediction.git
cd smart_home_energy_prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run notebooks in order
```bash
jupyter notebook notebooks/01_EDA.ipynb
```

---

## 📈 Key Results

- **18% accuracy improvement** over baseline via hyperparameter tuning
- **30% reduction** in training time through optimized feature selection
- Top features: `SquareFootage`, `Occupancy`, `HVACUsage`, `Temperature`
- HVAC usage alone accounts for ~22% of energy variance

---

## 🛠️ Tech Stack

`Python 3.10` · `Scikit-learn` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter`

---

## 👤 Author

**Yeddula Vishnu Raj**  
B.E. Computer Science & Engineering — Saveetha Institute of Medical and Technical Sciences  
📧 y.vishnuraj333@gmail.com  
