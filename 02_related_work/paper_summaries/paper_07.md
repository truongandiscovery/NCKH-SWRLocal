# Paper 07 Summary

## Citation

Tên bài: Applying Machine Learning and Statistical Forecasting Methods for Enhancing Pharmaceutical Sales Predictions

Tác giả: Konstantinos P. Fourkiotis, Athanasios Tsadiras

Năm: 2024

Nguồn: Forecasting, 6(1), pp. 170-186

DOI/Link: https://doi.org/10.3390/forecast6010010

## Problem

Bài báo giải quyết bài toán dự báo doanh số dược phẩm. Ngành dược cần dự báo chính xác để đảm bảo thuốc được sản xuất, phân phối và lưu trữ đúng nhu cầu. Nếu dự báo sai, doanh nghiệp có thể thiếu thuốc quan trọng hoặc tồn kho quá mức, ảnh hưởng đến chi phí, khả năng phục vụ và sức khỏe người dùng.

Các mô hình thống kê truyền thống như ARIMA, Exponential Smoothing hoặc Seasonal Naive có thể hữu ích, nhưng thường khó bắt được các mẫu phi tuyến, mùa vụ phức tạp và biến động khác nhau giữa các nhóm thuốc. Vì vậy, bài báo so sánh các phương pháp thống kê với ML/deep learning như XGBoost và LSTM.

## Method

Bài báo thực hiện quy trình gồm data cleaning, data transformation, ATC categorization, time-series analysis và forecasting. Dữ liệu được gom theo 8 nhóm thuốc dựa trên ATC Classification System.

Các phương pháp được so sánh gồm Seasonal Naive, Single/Double/Triple Exponential Smoothing, ARIMA, Facebook Prophet, XGBoost và LSTM neural network. Tác giả cũng thực hiện hyperparameter optimization bằng grid search để cải thiện dự báo.

## Dataset

Bài báo sử dụng dataset từ Kaggle gồm khoảng 600.000 bản ghi sales dược phẩm từ một pharmacy, giai đoạn 2014-2019. Dữ liệu ban đầu có độ phân giải hourly và được chuyển sang weekly time series để phù hợp hơn với phân tích xu hướng và chu kỳ vận hành.

Dataset được chia thành 8 drug categories theo ATC framework, ví dụ M01AB, M01AE, N02BA, N02BE, N05B, N05C và các nhóm thuốc khác. Quá trình xử lý dữ liệu gồm xử lý missing values, outliers, inconsistencies và chuẩn hóa dữ liệu.

## Evaluation

Bài báo đánh giá mô hình bằng:

- MAPE: sai số phần trăm tuyệt đối trung bình.
- MSE: sai số bình phương trung bình.

MAPE được nhấn mạnh vì dễ diễn giải trong bối cảnh doanh số dược phẩm, còn MSE giúp đo mức độ sai lệch tuyệt đối theo scale của từng nhóm thuốc.

## Results

Kết quả cho thấy XGBoost thường vượt trội hơn các phương pháp truyền thống trong nhiều nhóm thuốc. Ví dụ, với nhóm M01AB, XGBoost giảm MAPE từ 27.48% của Seasonal Naive xuống 17.89%. XGBoost cũng đạt MAPE 16.92% cho M01AE, 17.98% cho N02BA và 16.05% cho N02BE.

Về MSE, XGBoost đạt kết quả thấp ở nhiều nhóm như M01AB, N02BE và N05C. Facebook Prophet cũng có kết quả tốt cho dự báo dài hạn, ví dụ N05B có MAPE khoảng 18.39%. Bài báo kết luận rằng ML như XGBoost và LSTM giúp cải thiện độ chính xác dự báo trong ngành dược.

## Limitations

Một số hạn chế của bài báo:

- Dataset đến từ một pharmacy, nên khả năng khái quát cho toàn ngành dược còn hạn chế.
- Phần lớn phân tích là univariate time series, chưa khai thác nhiều external factors như thời tiết, dịch bệnh, khu vực, demographic hoặc chính sách y tế.
- Bài báo tập trung vào sales forecasting, chưa đánh giá trực tiếp inventory policy hoặc stockout/overstock.
- LSTM có thể cần dữ liệu lớn hơn và tuning kỹ hơn để phát huy hiệu quả.
- Các nhóm thuốc có scale khác nhau, nên so sánh MSE giữa nhóm cần cẩn thận.

## Relevance to our topic

Bài báo hữu ích cho đề tài nhóm vì cung cấp cách so sánh statistical forecasting và ML forecasting. Nhóm có thể tham khảo:

- Quy trình data cleaning và chuyển dữ liệu bán hàng thành weekly/daily time series.
- Cách so sánh Seasonal Naive, ARIMA, Prophet, XGBoost và LSTM.
- Cách dùng MAPE và MSE để đánh giá demand forecasting.
- Ý tưởng phân nhóm sản phẩm trước khi dự báo để cải thiện độ chính xác.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Áp dụng XGBoost cho dữ liệu warehouse/retail thay vì pharmaceutical sales.
- Kết hợp external features như promotion, holiday, season, lead time và current stock.
- Thêm module inventory recommendation sau khi có predicted demand.
- Đánh giá bằng cả forecasting metrics và business metrics như stockout rate hoặc inventory turnover.
- Thử group-based model theo product category để so sánh với global model.
