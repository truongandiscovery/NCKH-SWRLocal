# Topic Proposal

## 1. Proposed Title

**English title:**

Smart Warehouse Management System Using Machine Learning for Demand Forecasting and Inventory Recommendation

**Vietnamese title:**

Hệ thống quản lý kho thông minh sử dụng Machine Learning để dự báo nhu cầu và gợi ý nhập hàng

---

## 2. Application Domain

The application domain of this topic is **warehouse management and inventory management**.

The system focuses on supporting businesses in managing products, monitoring stock levels, forecasting product demand, and recommending suitable inventory decisions.

---

## 3. Real-World Problem

In traditional warehouse management, inventory decisions are often made manually based on experience or simple sales reports. This may lead to several problems:

- Products may be out of stock when customer demand increases.
- Some products may be overstocked, causing storage cost and capital waste.
- Managers may not know which products need to be imported soon.
- Demand changes over time, making manual forecasting inaccurate.
- Small and medium businesses may lack intelligent tools for inventory planning.

Therefore, a smart warehouse management system is needed to support more accurate and data-driven inventory decisions.

---

## 4. Target Users

The main target users of the system include:

- Warehouse managers.
- Inventory staff.
- Business owners.
- Sales and operation managers.
- Small and medium-sized enterprises that need inventory planning support.

---

## 5. Reason for AI Integration

AI should be integrated into the system because warehouse demand is affected by many factors, such as sales history, seasonal trends, product categories, and customer demand changes.

Machine Learning can help the system:

- Analyze historical sales and inventory data.
- Forecast future product demand.
- Detect products with high risk of stockout.
- Recommend suitable restocking quantities.
- Support managers in making faster and more accurate inventory decisions.

Without AI, the system can only store and display warehouse data. With AI, the system can provide prediction and recommendation functions, making it more useful for decision support.

---

## 6. Proposed AI Model / Method

The proposed AI methods include:

- **Random Forest Regressor** for demand forecasting.
- **XGBoost Regressor** as an alternative forecasting model.
- **Moving Average** as a baseline method for comparison.

The input data may include:

- Product ID.
- Product category.
- Historical sales quantity.
- Current stock quantity.
- Date or month.
- Previous demand values.
- Seasonal information.

The output of the model is:

- Predicted demand for each product.
- Recommended restocking quantity.
- Stockout risk warning.

---

## 7. Expected Results

The expected results of this topic are:

1. A smart warehouse management system that can manage products, stock-in, stock-out, and inventory status.
2. A Machine Learning module that can forecast future demand based on historical data.
3. An inventory recommendation function that suggests which products should be restocked.
4. A comparison between Machine Learning models and a traditional baseline method.
5. Evaluation results using metrics such as MAE, RMSE, and MAPE.
6. A dashboard that helps users monitor inventory status, predicted demand, and restocking recommendations.

---

## 8. Expected Contribution

This study is expected to contribute:

1. A practical system architecture for integrating Machine Learning into warehouse management.
2. A demand forecasting module to support inventory planning.
3. A restocking recommendation mechanism based on predicted demand and current stock.
4. An evaluation of Machine Learning effectiveness compared with a traditional forecasting baseline.
5. A simple and applicable solution for small and medium businesses to improve inventory decision-making.