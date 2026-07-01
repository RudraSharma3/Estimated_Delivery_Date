# 📦 Estimated Delivery Date (EDD) Prediction

A machine learning project focused on predicting the Estimated Delivery Date (EDD) for orders in an e-commerce setting. By leveraging historical shipment logs, the model forecasts transit days to minimize supply-chain ETA variance and improve logistics planning.

## 🚀 Project Overview
In e-commerce, accurate delivery estimates are crucial for operational efficiency and customer satisfaction. This project uses gradient boosting techniques to predict `predicted_exact_sla` — the exact number of days between an order being shipped and its actual delivery.

## 📊 Dataset & Scope
* **Source:** Internal e-commerce shipment and transit logs.
* **Scale:** 500K+ historical shipment records.
* **Core Features:** `shipment_mode`, `order_date`, `shipment_date`, `region_code`, `customer_pin`, `weight`, `volume`, and `product_category`.
* **Target Variable:** `predicted_exact_sla` (Integer number of days in transit).

## 🛠️ Tech Stack & Dependencies
The entire pipeline—from raw data processing to model evaluation—is self-contained and fully documented within a single Jupyter Notebook.
* **Language:** Python 🐍
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`, `seaborn`

## 🧠 Pipeline Architecture (Inside `EDD.ipynb`)
1. **Data Cleaning & Preprocessing:** Handled missing values, parsed raw datetime features, and normalized tabular distributions.
2. **Feature Engineering:** Extracted time-based and geographical constraints, introducing critical derivation features such as `shipping_duration`, `day_of_week`, and `distance_bucket`.
3. **Hyperparameter Tuning:** Executed an exhaustive Grid Search strategy across the XGBoost Regressor space to isolate optimal learning rates, tree depths, and estimators.
4. **Evaluation:** Diagnostic profiling using feature importance metrics, tracking predicted vs. actual SLA distributions.

## 📈 Model Performance Results
The optimized XGBoost Regressor model achieved high generalizable accuracy across the validation splits:
* **R² Score:** ~0.85
* **Mean Absolute Error (MAE):** ~1.2 days
* **Root Mean Squared Error (RMSE):** ~1.6 days

## 📂 Repository Structure
```text
.
├── EDD.ipynbtext          # Monolithic notebook containing EDA, Feature Engineering, and Modeling
└── README.md              # Project documentation
```
## 🙋‍♂️ Author
Rudra Sharma

Feel free to connect on LinkedIn or explore my other work on GitHub.
