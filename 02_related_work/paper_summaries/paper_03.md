# Paper 03 Summary

## Citation

Tên bài: A Comprehensive Study on Intelligent Inventory Management and Product Demand Forecasting Using Machine Learning Techniques

Tác giả: Shubha Rao V, Bindushree B, Deepak V, Achhutha Gowda N

Năm: 2026

Nguồn: International Journal of Applied Mathematics, Volume 39 No. 1s, 2026, pp. 85-96

DOI/Link: https://doi.org/10.12732/ijam.v39i1s.1613

## Problem

Bài báo giải quyết bài toán quản lý tồn kho và dự báo nhu cầu sản phẩm cho các cửa hàng bán lẻ nhỏ và vừa tại Ấn Độ. Các phương pháp truyền thống như ghi chép thủ công, dùng spreadsheet tĩnh hoặc dự báo dựa trên kinh nghiệm thường không phản ứng tốt với biến động nhu cầu theo mùa, ngày trong tuần, giá bán và các sự kiện văn hóa như lễ hội.

Vấn đề chính là nếu dự báo sai, cửa hàng có thể bị stockout làm mất doanh thu hoặc overstock làm tăng chi phí lưu kho, khóa vốn và gây lãng phí. Bài báo hướng đến một hệ thống nhẹ hơn ERP lớn nhưng vẫn đủ khả năng hỗ trợ quyết định nhập hàng dựa trên dữ liệu.

## Method

Bài báo đề xuất một hệ thống quản lý tồn kho thông minh tích hợp Machine Learning, gồm ba phần chính:

- Demand forecasting dựa trên dữ liệu bán hàng lịch sử, giá, mùa vụ, ngày trong tuần và lễ hội.
- Real-time stock monitoring, cảnh báo low-stock và gợi ý nhập hàng.
- Các chức năng vận hành như quản lý nhà cung cấp, procurement, dashboard, phân quyền Manager/Biller/Customer và đồng bộ đơn hàng online/offline.

Về mô hình, bài báo thử nghiệm Linear Regression, Random Forest, Support Vector Regression, XGBoost, LightGBM và CatBoost. Phần mô hình chính sử dụng ensemble gồm LightGBM, XGBoost và CatBoost. Các chiến lược ensemble được xét gồm simple averaging, R2 weighted averaging, RMSE optimized weighted averaging và stacking với Ridge Regression làm meta-learner.

## Dataset

Do không có dataset public phù hợp cho cửa hàng Kirana nhỏ và vừa tại Ấn Độ, tác giả tự tạo synthetic dataset bằng Python. Dataset mô phỏng giao dịch hằng ngày trong 2 năm, từ tháng 10/2023 đến tháng 10/2025.

Dataset gồm khoảng 36.500 dòng, 50 sản phẩm và 5 nhóm sản phẩm: Dairy, Beverages, Snacks, Staples và Personal Care. Mỗi bản ghi chứa thông tin sản phẩm, giá bán, tồn kho và số lượng bán hằng ngày.

Quá trình sinh dữ liệu xét đến nhiều yếu tố:

- Base demand bằng phân phối Poisson.
- Hệ số co giãn theo từng nhóm sản phẩm.
- Festival impact cho Diwali, Holi, Eid, Christmas.
- Seasonal modifiers, day-of-week effects và weekend effects.
- Biến động giá và khuyến mãi bằng Gaussian noise có kiểm soát.

Feature engineering gồm temporal features, lag features 1/3/7/14/21/30 ngày, rolling statistics, festival flags, festival proximity, discount features, category/product encoding và trend indicators.

## Evaluation

Bài báo đánh giá mô hình bằng các metric:

- RMSE: đo sai số bình phương trung bình căn bậc hai.
- MAE: đo sai số tuyệt đối trung bình.
- MAPE: đo sai số phần trăm tuyệt đối trung bình.
- R2: đo mức độ giải thích biến thiên của mô hình.

Tác giả dùng time-based train-validation split, trong đó 30 ngày cuối được dùng làm validation set. Cách chia này phù hợp với forecasting vì tránh đưa dữ liệu tương lai vào quá trình huấn luyện.

## Results

Kết quả chính là ensemble LightGBM + XGBoost + CatBoost đạt hiệu năng tốt nhất, với R2 xấp xỉ 0.96. CatBoost mạnh với biến phân loại và khác biệt theo nhóm sản phẩm, LightGBM đóng góp tốc độ và độ ổn định, còn XGBoost giúp bắt quan hệ phi tuyến và tương tác phức tạp.

Phân tích feature importance cho thấy các biến quan trọng nhất gồm lag sales, festival indicators, discount percent, rolling averages và seasonal variables. Điều này phù hợp với bối cảnh bán lẻ, nơi nhu cầu thường bị ảnh hưởng bởi chu kỳ thời gian, sự kiện, giá và khuyến mãi.

## Limitations

Một số hạn chế của bài báo:

- Dataset là dữ liệu tổng hợp, chưa kiểm chứng trực tiếp trên dữ liệu bán lẻ thực tế.
- Kết quả R2 xấp xỉ 0.96 khá cao nhưng bài báo chưa trình bày đầy đủ bảng kết quả chi tiết cho từng mô hình và từng nhóm sản phẩm.
- Chưa có đánh giá thực nghiệm về tác động kinh doanh như giảm stockout, giảm overstock, giảm holding cost hoặc tăng doanh thu.
- Chưa có triển khai thực tế với người dùng cuối để đánh giá tính dễ dùng và độ tin cậy của gợi ý nhập hàng.
- Bối cảnh nghiên cứu tập trung vào bán lẻ Ấn Độ, nên cần kiểm tra thêm nếu áp dụng cho quốc gia hoặc ngành hàng khác.

## Relevance to our topic

Bài báo liên quan trực tiếp đến đề tài Smart Warehouse Management System Using Machine Learning for Demand Forecasting and Inventory Recommendation.

Các điểm có thể tham khảo:

- Cách kết hợp demand forecasting với inventory recommendation.
- Cách tạo feature như lag sales, rolling average, season, weekday/weekend, discount và event indicators.
- Cách dùng boosting models như XGBoost, LightGBM, CatBoost cho dữ liệu tabular.
- Cách thiết kế dashboard, low-stock alert, procurement và supplier management.
- Cách đánh giá bằng MAE, RMSE, MAPE, R2 và có thể mở rộng sang metric nghiệp vụ.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Dùng dataset public hoặc dữ liệu mô phỏng có mô tả rõ quy tắc sinh dữ liệu.
- So sánh với baseline đơn giản như Moving Average, Seasonal Naive hoặc rule-based reorder point.
- Bổ sung business metrics như stockout rate, overstock rate, inventory turnover và service level.
- Kết hợp predicted demand với ROP, safety stock hoặc EOQ để tạo recommended restock quantity.
- Dùng SHAP hoặc feature importance để giải thích vì sao hệ thống gợi ý nhập hàng.
- Mở rộng từ retail sang warehouse với các thực thể như warehouse, supplier, import/export transaction, batch và lead time.
