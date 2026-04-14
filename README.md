# Supply-Chain-Demand-Forecasting-for-Stores-using-ML
This project focuses on forecasting product demand using machine learning techniques, aiming to support better material planning and supply-demand alignment in supply chain operations.

## 🔧 Tools & Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn

## 📊 Problem Statement
The objective is to predict `units_sold` based on historical weekly data. Accurate demand forecasting can significantly optimize inventory levels, reduce holding costs, and improve supply chain responsiveness.

## 📁 Dataset
The dataset contains ~10,000 records with features including:
- `product_id`
- `store_id`
- `week` (decomposed into `day`, `month`, `year`)
- `units_sold` (target variable)

## 🛠️ Data Preprocessing
- Removed null values
- Eliminated top 2% outliers in `units_sold` to reduce skewness
- Extracted temporal features (`day`, `month`, `year`) from the `week` column
- Dropped irrelevant columns (`record_ID`, original `week`)

## 🤖 Models Implemented
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

## ✅ Model Evaluation
Each model was evaluated using:
- **Root Mean Squared Error (RMSE)**
- **Adjusted R² Score**

| Model | RMSE | Adjusted R² |
|-------|------|-------------|
| Linear Regression | 32.92 | 0.2493 |
| Decision Tree     | 23.86 | 0.6055 |
| Random Forest     | 17.28 | 0.7932 |
| Gradient Boosting | 37.03 | 0.0497 |
| **XGBoost**       | **6.08** | **0.9209** ✅ |

## 🔍 Key Outcomes
- **XGBoost** outperformed all other models with the **lowest RMSE of 6.08** and **highest Adjusted R² of 0.9209**
- Demonstrated strong correlation between temporal features and demand patterns
- Showcased effective model comparison using quantitative metrics

## 📌 Conclusion
The XGBoost model offers a reliable and accurate method for demand forecasting. This solution can be extended to drive improvements in material availability, purchase planning, and supply chain efficiency.
