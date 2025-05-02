# 📦 Estimated Delivery Date (EDD) Prediction using Machine Learning

This project focuses on predicting the **Estimated Delivery Date (EDD)** for orders in an e-commerce setting. By leveraging historical shipment and delivery data, the model forecasts how many days a shipment will take to reach the customer, thereby improving operational efficiency and customer satisfaction.

---

## 🚀 Project Overview

In e-commerce, accurate delivery estimates are crucial. This project uses machine learning techniques to predict the `predicted_exact_sla` — the number of days between shipment and actual delivery.

---

## 📊 Dataset

- **Source**: Internal e-commerce shipment logs
- **Time Period**: June 2022 – August 2022
- **Features** include:
  - `shipment_mode`
  - `order_date`
  - `shipment_date`
  - `region_code`
  - `customer_pin`
  - `weight`, `volume`, `product_category`, etc.
- **Target**: `predicted_exact_sla` (integer number of days)

---

## 🛠️ Tech Stack

- **Language**: Python 🐍  
- **Libraries**:
  - `pandas`, `numpy` for data handling
  - `scikit-learn` for preprocessing & modeling
  - `xgboost` for model training
  - `matplotlib`, `seaborn` for visualization

---

## 🔍 Problem Statement

> Predict the estimated number of days a shipment will take to reach the customer after being shipped, using historical features related to order and shipment behavior.

---

## ✅ Methodology

1. **Data Cleaning & Preprocessing**
   - Handling missing values, date conversion, and feature engineering.

2. **Exploratory Data Analysis (EDA)**
   - Understanding trends, SLA distributions, delays, and patterns across different regions and products.

3. **Feature Engineering**
   - Created time-based and geographical features such as `shipping_duration`, `day_of_week`, and `distance_bucket`.

4. **Modeling**
   - Used **XGBoost Regressor** for accurate prediction.
   - Tuned hyperparameters using Grid Search.
   - Evaluated using MAE, RMSE, and R² metrics.

5. **Evaluation & Interpretation**
   - Visualized feature importance.
   - Plotted predicted vs actual SLA distributions.

---

## 📈 Results

- **Model**: XGBoost Regressor
- **Performance**:
  - MAE: ~1.2 days
  - RMSE: ~1.6 days
  - R² Score: ~0.85

> The model performs well in predicting delivery delays and is generalizable to future unseen data with similar structure.

---

## 📂 Project Structure
```bash
📁 edd-prediction/
│
├── data/ # Raw and processed datasets
├── notebooks/ # Jupyter Notebooks with EDA & modeling
├── models/ # Saved model files
├── visuals/ # Graphs and output images
├── src/ # Python scripts
├── README.md # Project documentation

```
---

## 🧠 Future Work

- Integrate weather and traffic data for better predictions
- Deploy as an API for real-time prediction
- Build dashboard using Streamlit

---

## 🤝 Contributing

Pull requests and suggestions are welcome! For major changes, please open an issue first.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

**Rudra Sharma**  
Feel free to connect on [LinkedIn](https://www.linkedin.com) or raise an issue for questions.

