# Topic Proposal

## 1. Group Information

- Class:
- Group:
- Leader:
- Members:

## 2. Proposed Title

**English title:**

Smart Warehouse Management System Using Machine Learning for Demand Forecasting and Inventory Recommendation

**Vietnamese title:**

Hệ thống quản lý kho thông minh sử dụng Machine Learning để dự báo nhu cầu và gợi ý nhập hàng

## 3. Application Domain

The application domain of this topic is **warehouse management and inventory management**.

This topic focuses on applying Machine Learning to support warehouse managers in monitoring inventory, forecasting product demand, and making better restocking decisions.

## 4. Problem Statement

In traditional warehouse management, inventory decisions are often made manually based on experience or simple sales reports. This may cause several problems such as stock shortage, overstocking, inaccurate demand estimation, and inefficient restocking decisions.

When customer demand changes over time, managers may find it difficult to decide which products should be imported, how many items should be restocked, and when restocking should be done. As a result, businesses may lose sales opportunities due to stockouts or waste storage costs due to excessive inventory.

Therefore, a smart warehouse management system is needed to support demand forecasting and inventory recommendation using historical sales and stock data.

## 5. Motivation

Warehouse management is an important part of business operations, especially for retail stores, supermarkets, and small or medium-sized enterprises. Poor inventory planning can directly affect revenue, customer satisfaction, and operating costs.

By integrating Machine Learning into a warehouse management system, the system can analyze historical data, forecast future demand, and suggest suitable restocking quantities. This helps managers make faster and more data-driven decisions instead of relying only on manual experience.

## 6. Target Users

The main target users of the system include:

- Warehouse managers.
- Inventory staff.
- Business owners.
- Sales and operation managers.
- Small and medium-sized enterprises that need inventory planning support.

## 7. Proposed AI Model / Method

The proposed AI methods include:

- **Random Forest Regressor** for product demand forecasting.
- **XGBoost Regressor** as an alternative Machine Learning model.
- **Moving Average** as a traditional baseline method for comparison.

The input data may include:

- Product ID.
- Product category.
- Historical sales quantity.
- Current stock quantity.
- Date, month, or season.
- Previous demand values.

The output of the AI model includes:

- Predicted demand for each product.
- Recommended restocking quantity.
- Stockout risk warning.

## 8. System Features

The main features of the system include:

1. Product and inventory management.
2. Stock-in and stock-out transaction management.
3. Demand forecasting using Machine Learning.
4. Inventory recommendation and restocking suggestion.
5. Low-stock and stockout risk warning.
6. Dashboard for inventory status, predicted demand, and recommendation results.

## 9. Expected Contribution

The expected contributions of this study are:

1. Propose a smart warehouse management system architecture integrated with Machine Learning.
2. Develop a demand forecasting module based on historical sales and inventory data.
3. Build an inventory recommendation mechanism to support restocking decisions.
4. Compare Machine Learning models with a traditional baseline method.
5. Evaluate the effectiveness of the proposed system using forecasting metrics.

## 10. Evaluation Plan

The system will be evaluated based on forecasting performance and usefulness of inventory recommendations.

- **Dataset:** Historical sales and inventory data. The group may use a public retail dataset, such as Online Retail Dataset or Superstore Dataset, or create a simulated warehouse dataset if real data is not available.
- **Baseline:** Moving Average method or simple rule-based restocking method.
- **Metrics:** MAE, RMSE, MAPE for demand forecasting; stockout reduction and overstock reduction for inventory recommendation.
- **Expert evaluation:** Warehouse staff, business owners, or instructors may review whether the recommendations are reasonable.
- **User survey:** Users may evaluate the system based on usefulness, ease of use, and decision support effectiveness.

## 11. Related Papers

To be updated.