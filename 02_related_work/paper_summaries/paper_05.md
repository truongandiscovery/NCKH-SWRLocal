# Paper 05 Summary

## Citation

Tên bài: Research on Inventory Forecasting and Management Strategies in Logistics and Warehousing Automation Based on Artificial Intelligence Models

Tác giả: Zhicheng Ma

Năm: 2025

Nguồn: Journal of Combinatorial Mathematics and Combinatorial Computing, Volume 124

DOI/Link: https://combinatorialpress.com/jcmcc-articles/volume-124/research-on-inventory-forecasting-and-management-strategies-in-logistics-and-warehousing-automation-based-on-artificial-intelligence-models/

## Problem

Bài báo giải quyết vấn đề dự báo tồn kho và quản lý kho trong logistics/warehousing automation. Trong kho vận, nếu không dự báo chính xác lượng tồn kho và không cập nhật kịp thời luồng hàng nhập/xuất, doanh nghiệp dễ gặp backlog, stockout, mất mát hàng hóa, chi phí vận hành cao và phản hồi chậm với yêu cầu người dùng.

Bài báo muốn chứng minh rằng mô hình AI có thể hỗ trợ inventory forecasting và warehouse management tốt hơn các hướng công nghệ riêng lẻ như IoT hoặc blockchain trong một số tiêu chí vận hành.

## Method

Bài báo sử dụng Least Squares Support Vector Machine (LSSVM) để xây dựng mô hình dự báo inventory. Mô hình chuyển bài toán phi tuyến sang không gian đặc trưng cao chiều bằng kernel function, sau đó tối ưu theo nguyên lý structural risk minimization.

Ngoài mô hình dự báo, bài báo đề xuất kiến trúc automation cho logistics warehousing gồm nhiều lớp như user layer, front-end control, back-end service, data persistence và data storage. Hệ thống có các interface cho nhập kho, xuất kho, truy vấn hàng hóa và kết nối với enterprise resource management system qua giao thức HTTP/data retrieval.

## Dataset

Bài báo không công bố một dataset public cụ thể. Dữ liệu thử nghiệm được mô tả là dữ liệu thu thập từ hệ thống warehousing logistics trong môi trường kiểm thử. Phần test preparation mô tả thiết bị như data processing equipment, data acquisition equipment, barcode scanning và automated guided vehicles.

Các bảng kết quả sử dụng một số mẫu actual inventory và predicted inventory để so sánh giữa AI technology, IoT technology và blockchain technology. Ví dụ, ở lần dự báo đầu tiên actual inventory là 230, AI dự báo 229, IoT dự báo 210 và blockchain dự báo 240.

## Evaluation

Bài báo đánh giá theo các tiêu chí vận hành:

- Inventory forecasting accuracy: so sánh predicted inventory với actual inventory.
- Inventory turnover efficiency: số lần quay vòng tồn kho mỗi tháng.
- Response speed: thời gian phản hồi của hệ thống dự báo/quản lý.
- Order processing time: thời gian xử lý đơn hàng từ inbound đến outbound.

Các phương pháp được so sánh gồm AI technology, IoT technology và blockchain technology.

## Results

Kết quả cho thấy AI technology dự báo gần actual inventory hơn IoT và blockchain. Trong các ví dụ được trình bày, AI thường lệch rất nhỏ, chẳng hạn 229 so với actual 230, 245 so với actual 245, 220 so với actual 220.

Về turnover efficiency, AI đạt mức cao hơn trong nhiều tháng, ví dụ 5-6 lần/tháng ở một số tháng. Về response speed, AI thường phản hồi khoảng 2-5 giây, nhanh hơn IoT và blockchain trong nhiều lần kiểm thử. Về order processing time, AI xử lý khoảng 8.7-10.1 giây, trong khi IoT và blockchain thường lâu hơn.

## Limitations

Một số hạn chế của bài báo:

- Dataset và quy trình thu thập dữ liệu chưa được mô tả đủ chi tiết.
- Số mẫu thử nghiệm trong bảng còn nhỏ, khó đánh giá độ tin cậy thống kê.
- So sánh AI, IoT và blockchain chưa thật sự tương đương vì AI là phương pháp dự báo, còn IoT/blockchain là công nghệ hạ tầng.
- Không có train/test split rõ ràng, không có metric phổ biến như MAE, RMSE, MAPE.
- Chưa có phân tích chi phí triển khai hoặc độ phức tạp vận hành thực tế.

## Relevance to our topic

Bài báo liên quan đến đề tài của nhóm ở phần inventory forecasting, warehouse automation và real-time inventory management. Nhóm có thể tham khảo:

- Ý tưởng dùng AI để dự báo tồn kho và hỗ trợ nhập hàng.
- Các metric vận hành như response speed, order processing time và inventory turnover.
- Kiến trúc nhiều lớp cho hệ thống quản lý kho.
- Cách kết nối module warehouse với hệ thống ERP hoặc supplier system.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Dùng dataset rõ ràng và công khai để đánh giá mô hình.
- Thay LSSVM bằng các mô hình dễ triển khai hơn như Random Forest, XGBoost hoặc LightGBM.
- Bổ sung MAE, RMSE, MAPE, R2 để đánh giá forecasting.
- Tách rõ vai trò của AI model, IoT tracking và blockchain traceability.
- Xây dựng prototype có nhập kho, xuất kho, cảnh báo low-stock và recommended restock quantity.
