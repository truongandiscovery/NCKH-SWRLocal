# Paper 08 Summary

## Citation

Tên bài: Digital Infrastructure for Predictive Inventory Management in Retail Using Machine Learning

Tác giả: Raviteja Meda

Năm: 2021

Nguồn: International Journal of Advanced Research in Computer and Communication Engineering (IJARCCE), Vol. 10, Issue 12, December 2021

DOI/Link: https://doi.org/10.17148/IJARCCE.2021.101276

## Problem

Bài báo giải quyết vấn đề xây dựng hạ tầng số cho predictive inventory management trong retail. Retailers có nhiều dữ liệu như POS, inventory level, shipment, promotion, forecast, weather và customer behavior, nhưng nếu thiếu hạ tầng dữ liệu phù hợp thì rất khó dùng ML để dự báo nhu cầu và đề xuất replenishment.

Mục tiêu của bài báo là trình bày một digital infrastructure có thể dự báo demand theo daily/article-store level và đưa ra lời khuyên đặt hàng để tránh stockout, đồng thời vẫn có thể triển khai với chi phí thấp hoặc vừa phải.

## Method

Bài báo đề xuất một kiến trúc digital infrastructure cho predictive inventory management. Các thành phần chính gồm:

- Data architecture: pipeline cho data engineering, data mining, batch/stream processing.
- Business applications: dashboard, forecasting, clustering, replenishment advising.
- Cloud architecture: hạ tầng scalable để train/serve ML model.
- Coalition/governance: phối hợp giữa business users, data engineers, data scientists và decision makers.

Hệ thống sử dụng ML để dự báo sales/demand và kết hợp với replenishment order advising. Bài báo cũng thảo luận các hướng như supervised learning, unsupervised learning, reinforcement learning, feature engineering, real-time update, API và performance monitoring.

## Dataset

Bài báo mô tả việc đánh giá qua simulation process dựa trên dữ liệu từ một large retail store và on-field operation tại một smaller retail store. Nguồn dữ liệu được nhắc đến gồm historical sales, inventory level, shipment, forecast data, weather, holiday, promotion, customer/supplier data và các dữ liệu vận hành retail.

Tuy nhiên, bài báo không công bố dataset chi tiết, số dòng, danh sách biến đầy đủ hoặc dữ liệu raw để tái lập.

## Evaluation

Bài báo đánh giá hệ thống thông qua simulation và field operation. Các tiêu chí đánh giá gồm:

- Forecasting accuracy.
- Filling rate/service level.
- Stockout analysis.
- Sales increase.
- Cost decrease.
- Khả năng theo dõi forecast error và model performance theo thời gian.
- Khả năng đề xuất replenishment quantity cho article-store-week.

## Results

Bài báo cho rằng digital structure đề xuất có performance tốt trong cả simulation và field operation, với sales increase và cost decrease đáng kể. Hệ thống có thể dự báo future sales theo article-store-week và đề xuất replenishment quantities để giữ stock levels trong một khoảng mong muốn.

Bài báo cũng nhấn mạnh lợi ích dài hạn của kiến trúc: real-time stock/sales updates, API phục vụ người dùng cuối, lưu trữ input/output của model để theo dõi performance, dễ thay đổi model hoặc feature engineering trong tương lai.

## Limitations

Một số hạn chế của bài báo:

- Chi tiết dataset và kết quả định lượng chưa được trình bày rõ, khó tái lập.
- Bài báo thiên về framework/infrastructure hơn là thực nghiệm mô hình cụ thể.
- Việc triển khai hạ tầng số có thể tạo thay đổi lớn trong information flow và cấu trúc công việc của retailer.
- Có rủi ro về data quality, integration, training nhân sự và độ ổn định vận hành.
- Chưa nêu rõ model nào đạt kết quả tốt nhất trong các tình huống cụ thể.

## Relevance to our topic

Bài báo liên quan đến đề tài nhóm ở phần hệ thống. Nhóm không chỉ cần model dự báo mà còn cần hạ tầng để đưa model vào warehouse management system:

- Data pipeline cho sales/inventory data.
- Dashboard cho current stock, forecast và recommendation.
- API hoặc service để chạy model và lưu kết quả dự báo.
- Theo dõi forecast error theo thời gian.
- Replenishment advising dựa trên predicted demand.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Xây dựng prototype nhỏ nhưng rõ ràng với database, model service và dashboard.
- Công bố schema dữ liệu: product, stock transaction, sales order, supplier, forecast result.
- Dùng model cụ thể như Random Forest hoặc XGBoost thay vì chỉ mô tả framework.
- Đưa ra công thức recommended restock quantity.
- Đánh giá bằng MAE/RMSE/MAPE và inventory KPIs.
- Thiết kế hệ thống đơn giản hơn để phù hợp với SMEs.
