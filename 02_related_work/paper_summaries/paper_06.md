# Paper 06 Summary

## Citation

Tên bài: AI-Powered Forecasting for Supply Chain Resilience: Applications of Logistic Regression, Random Forest, and XGBoost in the U.S. Context

Tác giả: Abdullah Sheikh, Kendall Goodrich, Susmitha Sajja

Năm: 2025

Nguồn: American Journal of Innovation in Science and Engineering, 4(3), pp. 105-117

DOI/Link: https://doi.org/10.54536/ajise.v4i3.6065

## Problem

Bài báo giải quyết vấn đề tăng khả năng chống chịu của chuỗi cung ứng Hoa Kỳ trước các biến động như đại dịch, xung đột địa chính trị, biến đổi khí hậu, biến động nhiên liệu và nhu cầu khách hàng thay đổi nhanh. Các mô hình truyền thống như ARIMA và Exponential Smoothing vẫn được dùng rộng rãi nhưng khó xử lý quan hệ phi tuyến và dữ liệu nhiều nguồn.

Mục tiêu của bài báo là so sánh các mô hình ML gồm Logistic Regression, Random Forest và XGBoost với mô hình truyền thống để xem mô hình nào giúp cải thiện forecast accuracy, giảm chi phí tồn kho, tăng service reliability và hỗ trợ logistics efficiency.

## Method

Bài báo dùng quy trình thực nghiệm gồm data collection, preprocessing, model training và comparative evaluation. Các mô hình được thử nghiệm:

- Logistic Regression: dùng như baseline ML có tính dễ giải thích.
- Random Forest: ensemble decision trees, xử lý noise và giảm overfitting.
- XGBoost: boosting-based model, tối ưu lỗi theo từng vòng lặp và xử lý feature tương tác tốt.
- Baseline truyền thống: ARIMA, ETS và Seasonal Naive.

Preprocessing gồm xử lý missing values bằng mean/mode imputation, loại outlier bằng z-score filtering, feature selection bằng correlation analysis và mutual information, sau đó normalization bằng min-max scaling.

## Dataset

Bài báo sử dụng Walmart Kaggle dataset để đánh giá demand forecasting trong retail. Ngoài ra, tác giả còn dùng các nguồn dữ liệu thứ cấp/open-access liên quan đến retail demand và logistics operations tại Hoa Kỳ.

Các biến đầu vào được mô tả gồm demand signals, supplier lead times, inventory inflow/outflow, fuel prices, weather và các yếu tố exogenous khác. Dữ liệu được dùng để đánh giá cả forecasting accuracy lẫn tác động vận hành như inventory cost, fill rate và routing/fuel efficiency.

## Evaluation

Bài báo đánh giá theo hai nhóm chỉ số:

- Forecasting metrics: forecast error, MAPE/error reduction so với baseline.
- Operational metrics: inventory cost reduction, fill rate/service level, routing inefficiency và fuel cost reduction.

Điểm mạnh của bài báo là không chỉ đánh giá mô hình dự báo theo sai số, mà còn liên hệ forecast accuracy với hiệu quả tồn kho và logistics.

## Results

Kết quả cho thấy XGBoost vượt trội hơn các mô hình khác. Trên Walmart Kaggle dataset, XGBoost đạt mức giảm MAPE khoảng 56% so với baseline và giảm inventory cost khoảng 35.7%. Bài báo cũng báo cáo fill rate đạt trên 95% và fuel cost giảm khoảng 14%.

Random Forest cho kết quả trung bình, có cải thiện nhưng không ổn định bằng XGBoost. Logistic Regression dễ giải thích nhưng thường kém hơn trong bối cảnh demand phi tuyến và biến động mạnh. Bài báo kết luận rằng ensemble/boosting methods có giá trị chiến lược trong forecasting và supply chain resilience.

## Limitations

Một số hạn chế của bài báo:

- Dữ liệu chủ yếu là secondary/open-access data, thiếu dữ liệu ERP/supplier transaction real-time độc quyền.
- Kết quả phụ thuộc vào Walmart dataset, có thể chưa đại diện cho mọi ngành.
- XGBoost mạnh nhưng khó giải thích hơn Logistic Regression, gây khó khăn khi triển khai trong môi trường cần transparency.
- Chưa đánh giá sâu black-swan events hoặc structural breaks cực đoan.
- Một số kết quả có tính tổng hợp từ published studies, nên cần thận trọng khi tái lập.

## Relevance to our topic

Bài báo liên quan trực tiếp vì nhóm cũng cần dự báo nhu cầu và gợi ý nhập hàng. Nhóm có thể tham khảo:

- Cách dùng XGBoost cho retail/warehouse demand forecasting.
- Cách so sánh với baseline như Seasonal Naive hoặc ARIMA.
- Cách liên kết forecast error với inventory cost, fill rate và service level.
- Cách đưa external features như weather, fuel price, lead time vào mô hình.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Dùng XGBoost làm model chính và so sánh với Random Forest, Moving Average.
- Bổ sung SHAP để giải thích mô hình XGBoost.
- Tập trung vào warehouse-specific metrics như stockout rate, overstock rate và reorder recommendation accuracy.
- Dùng dataset nhỏ hơn nhưng mô phỏng rõ current stock, lead time và reorder point.
- Tạo module cảnh báo khi predicted demand vượt current stock + incoming stock.
