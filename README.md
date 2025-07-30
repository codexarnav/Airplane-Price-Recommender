# ✈️ Flight Price Optimizer

This project predicts flight demand and recommends **optimal seat prices** to help airlines **maximize revenue**. It combines machine learning with price-demand simulation to provide actionable pricing strategies.

---

## 🚀 Features

- 🔍 Predicts demand based on input features (airline, route, duration, etc.)
- 📈 Simulates revenue at different seat price points
- 🧠 Uses XGBoost regression for demand prediction
- 📊 Visualizes price vs demand and revenue using Streamlit
- 💰 Recommends the **best seat price** for revenue maximization

---
## 🧠 ML Model Details

- Model: `XGBoostRegressor`
- Tuning: `Optuna` used to optimize parameters like learning rate, max depth, etc.
- Input Features:
  - Airline (encoded)
  - Class (Economy/Business)
  - Duration (in minutes)
  - Departure Hour
  - Arrival Hour
  - Route (encoded)
- Output: Predicted passenger **demand**
- Revenue = `Seat Price × Predicted Demand`

---

## 📈 Sample Output

```python
Input:
{
    'airline': 1,
    'class': 1,
    'duration_mins': 150,
    'dep_hour': 9,
    'arr_hour': 11,
    'route': 14
}

Prediction:
Predicted Demand: 125.55 passengers

## 📦 Installation

1. **Clone the repo**
```bash
git clone https://github.com/yourusername/flight-price-optimizer.git
cd flight-price-optimizer

pip install -r requirements.txt
