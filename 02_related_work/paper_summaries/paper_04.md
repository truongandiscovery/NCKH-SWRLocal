# Paper 04 Summary

## Citation

Tên bài: Forecasting and Inventory Planning: An Empirical Investigation of Classical and Machine Learning Approaches for Svanehøj's Future Software Consolidation

Tác giả: Hadid J. Wahedi, Mads Heltoft, Glenn J. Christophersen, Thomas Severinsen, Subrata Saha, Izabela Ewa Nielsen

Năm: 2023

Nguồn: Applied Sciences, 13(15), 8581

DOI/Link: https://doi.org/10.3390/app13158581

## Problem

Bài báo giải quyết vấn đề forecasting và inventory planning trong SME sản xuất. Nhiều doanh nghiệp nhỏ và vừa vẫn dựa vào ERP, MRP, reorder point hoặc dự báo định tính từ kinh nghiệm sales. Cách làm này dễ tạo khoảng cách giữa dự báo nhu cầu, lập kế hoạch mua hàng và kiểm soát tồn kho.

Trong case Svanehøj Danmark A/S, doanh nghiệp gặp vấn đề tồn kho cao và stockout với các raw materials/sub-components quan trọng. Bài báo đặt câu hỏi liệu các mô hình Machine Learning và Reinforcement Learning có thể hỗ trợ forecasting và inventory planning tốt hơn các phương pháp thống kê/truyền thống trong bối cảnh SME hay không.

## Method

Bài báo triển khai một empirical case study với dữ liệu ERP của một công ty SME Đan Mạch. Phần forecasting so sánh các mô hình thống kê và ML, gồm Simple Exponential Smoothing (SES), ARIMA, ANN, LSTM, SVR, Random Forest, Wavelet-ANN và Wavelet-LSTM.

Phần inventory planning so sánh các cách ra quyết định tồn kho như actual practice của doanh nghiệp, EOQ, Q-learning và Deep Q Network (DQN). Các mô hình được triển khai bằng Python/TensorFlow và được đánh giá không chỉ theo forecast accuracy mà còn theo KPI vận hành/quản trị.

## Dataset

Dataset được trích từ hệ thống ERP Microsoft Dynamics AX của Svanehøj Danmark A/S. Dữ liệu gồm cả biến categorical và numerical, liên quan đến BOM, supplier information, demand, inventory và purchasing.

Nghiên cứu chọn 3 sub-components quan trọng được dùng trong nhiều finished products. Dữ liệu được aggregate theo tháng thành time series gồm 46 data points, từ tháng 04/2019 đến tháng 01/2023. Với các mô hình ML, tác giả chia dữ liệu theo tỷ lệ 80:20 cho train/test.

## Evaluation

Bài báo đánh giá theo hai nhóm metric:

- Forecasting metrics: các chỉ số sai số dự báo như MAE, RMSE, MAPE và các đánh giá thống kê liên quan.
- Inventory/managerial KPIs: total profit, inventory level, holding cost, stockout/backorder, fill rate và các chỉ số chi phí trong chính sách replenishment.

Điểm đáng chú ý là bài báo nhấn mạnh sự khác biệt giữa academic accuracy và managerial performance. Một mô hình dự báo có sai số thấp chưa chắc tạo ra chính sách tồn kho tốt nhất nếu xét theo chi phí và lợi nhuận.

## Results

Kết quả cho thấy nhiều mô hình ML có thể tốt hơn các phương pháp thống kê cổ điển về forecasting. Tuy nhiên, không có một mô hình forecast nào luôn tốt nhất cho mọi item. Hiệu quả phụ thuộc vào dữ liệu đầu vào, hyperparameter và đặc điểm demand của từng sản phẩm.

Ở phần inventory planning, Q-learning đạt kết quả kinh tế tốt nhất trong các kịch bản thử nghiệm. Q-learning giữ tồn kho ở mức thấp hơn nhưng vẫn cân bằng order quantity với demand, dẫn đến total profit tốt hơn actual practice, EOQ và DQN. DQN phức tạp hơn nhưng không cho cải thiện rõ ràng so với Q-learning.

## Limitations

Một số hạn chế của bài báo:

- Case study chỉ thực hiện trên một SME và 3 sub-components, nên khả năng khái quát còn hạn chế.
- Dữ liệu được aggregate theo tháng, có thể mất thông tin chi tiết theo ngày/tuần.
- Raw data không được công bố rộng rãi, chỉ có thể yêu cầu từ tác giả.
- Chưa đánh giá multi-echelon inventory hoặc mạng lưới kho/phân phối phức tạp.
- Mô hình RL cần nhiều kiến thức kỹ thuật và tài nguyên tính toán, có thể khó triển khai ngay trong SME.

## Relevance to our topic

Bài báo rất gần với đề tài của nhóm vì kết hợp demand forecasting và inventory planning. Nhóm có thể học cách:

- So sánh model dự báo với baseline thống kê.
- Đánh giá không chỉ bằng MAE/RMSE/MAPE mà còn bằng inventory KPIs.
- Kết nối predicted demand với chính sách nhập hàng.
- Nhìn hệ thống ML như một extension cho ERP/warehouse management system.

## Possible improvement

Nhóm có thể mở rộng bằng cách:

- Áp dụng dữ liệu retail/warehouse public để tăng khả năng tái lập.
- Dùng Random Forest/XGBoost làm mô hình chính trước khi thử RL phức tạp.
- Bổ sung reorder point, safety stock và recommended restock quantity.
- Tạo dashboard so sánh current stock, predicted demand và suggested order.
- Đánh giá song song forecasting metrics và business metrics như stockout rate, overstock rate, inventory turnover.
