# Time-Series-Forecasting
This project focuses on time series forecasting of daily revenue using historical transactional data. The dataset includes date-wise revenue generated, and we forecast future revenue using XGBoost with engineered time-based features.

---

## 📊 Objective

To build a predictive model that forecasts revenue using time-based features derived from transactional data such as:

- Year
- Month
- Day
- Day of Week
- Day of Year
- Hour
- Quarter

---

## 📁 Dataset

- **Source**: [Ecommerce Data – Kaggle](https://www.kaggle.com/datasets/carrie1/ecommerce-data)
- **Description**: This dataset contains transactional data for a UK-based online retail store, including invoice details, quantities, prices, timestamps, and customer information.

---

## 🧰 Tools & Libraries

- **Python**
- **Pandas**, **NumPy** – data processing
- **Matplotlib**, **Seaborn** – visualization
- **XGBoost** – modeling
- **Scikit-learn** – metrics

---

## ⚙️ Workflow

1. **Data Cleaning**:
   - Removed negative/zero `Quantity` and `UnitPrice`.
   - Calculated `Revenue = Quantity × UnitPrice`.
   - Set `InvoiceDate` as datetime index.

2. **Outlier Removal**:
   - Used IQR method to filter extreme revenue values.

3. **Feature Engineering**:
   - Extracted time-based features: year, month, day, etc.

4. **Train-Test Split**:
   - Train: data before `2011-10-01`
   - Test: data from `2011-10-01` onwards

5. **Model Training**:
   - XGBoost with early stopping and low learning rate.

6. **Evaluation**:
   - Root Mean Squared Error (RMSE)
   - Plots for actual vs predicted revenue

---

## 📈 Results

- **Model**: XGBoost Regressor
- **Evaluation Metric**: RMSE
- Visuals: Time plots of predictions vs actual values

---

## 📷 Sample Visualizations

<img width="986" height="451" alt="image" src="https://github.com/user-attachments/assets/40f82395-e71b-49ee-9665-4400f0642f1a" />
