# Paper 01 Summary

## Citation

Tên bài: Optimizing warehouse management system with blockchain and machine learning predictive data analytics

Tác giả: Kapil N. Hande, Manoj B. Chandak

Năm: 2024

Nguồn: International Journal of Informatics and Communication Technology (IJ-ICT)

DOI/Link: https://iaesjournal.org/index.php/ijict/article/view/2912

## Problem

Bài báo giải quyết các hạn chế của hệ thống quản lý kho (WMS) truyền thống. Các hệ thống cũ chủ yếu phụ thuộc vào cơ sở dữ liệu tập trung, dẫn đến rủi ro dễ bị giả mạo dữ liệu và thiếu khả năng tương tác đồng bộ giữa các thực thể khác nhau trong chuỗi cung ứng.

Bên cạnh đó, khi quy mô hoạt động của kho bãi ngày càng mở rộng, việc quản lý đòi hỏi phải giải quyết nhanh chóng các bài toán phức tạp như: dự báo nhu cầu khách hàng không ổn định, tối ưu hóa không gian, tối ưu hóa tuyến đường, và lên lịch giao hàng. Việc ứng dụng các công nghệ phân tán (như Blockchain) có thể giải quyết bài toán minh bạch, nhưng lại đòi hỏi phải thay đổi hoặc thay thế hoàn toàn hệ thống hiện tại.

## Method

Bài báo đề xuất khung hệ thống quản lý kho thông minh trên nền tảng Web3, gọi tắt là SWMW3 (Smart Warehouse Management in Web3). Hệ thống này tích hợp 3 thành phần công nghệ cốt lõi:

- Phát triển Web (MERN Stack): Hệ thống là một ứng dụng phi tập trung (DApp) với giao diện người dùng (frontend) được xây dựng bằng ReactJS và máy chủ (backend) sử dụng ExpressJS.
- Blockchain & Smart Contracts: Sử dụng Ganache, Truffle, Solidity và Web3js để tạo mạng lưới blockchain riêng tư. Hợp đồng thông minh (Smart contracts) được dùng để tự động hóa việc theo dõi hàng hóa, đối soát hóa đơn và thực hiện các giao dịch một cách minh bạch, bất biến. Hàng hóa được gán mã vạch (tạo bằng react-barcode) để tạo thành các "bản sao kỹ thuật số" (digital twins) ghi nhận trực tiếp lên blockchain.
- Machine Learning (Học máy): Tích hợp mô hình mạng nơ-ron bộ nhớ ngắn hạn dài (Long Short-Term Memory - LSTM) xây dựng bằng Python (TensorFlow). Mô hình được lưu dưới định dạng HDF5, sau đó load thẳng vào hệ thống backend thông qua TensorFlow.js (TFJS) để phục vụ cho phân tích dữ liệu dự đoán thời gian thực.

## Dataset

Nghiên cứu sử dụng một tập dữ liệu nền tảng lấy từ Kaggle. Do cần kiểm chứng cả luồng dữ liệu giao dịch và luồng dữ liệu học máy, nhóm tác giả đã xây dựng một thuật toán tạo dữ liệu mô phỏng (GenData).

Thuật toán này tự động tạo ra các đặc trưng quan trọng cho từng mặt hàng (SKU) bao gồm: loại mặt hàng, số lượng, thời gian hàng đến (arrival time) và thời gian xuất kho ngẫu nhiên (departure time). Các dữ liệu này được ánh xạ với một mã vạch (barcode) để tạo thành chuỗi thông tin hoàn chỉnh, phục vụ cho việc ghi block trên blockchain và làm tập huấn luyện (training data) cho mô hình ML.

## Evaluation

Thay vì chỉ đánh giá mô hình học máy bằng các độ đo sai số thuần túy (như RMSE, MAE), bài báo này đánh giá tổng thể khả năng triển khai thực tế của toàn bộ kiến trúc phần mềm.

Khả năng vận hành của hệ thống được đánh giá thông qua việc kiểm thử các giao diện và luồng nghiệp vụ thực tế như: quản lý nhập kho (inbound management), quản lý tồn kho, đăng ký nhân sự và nhà cung cấp. Mô hình học máy LSTM được đánh giá định tính là đã dự đoán chính xác tổng thời gian từ khi nhận đơn đến lúc xuất xưởng.

## Results

Kết quả chính của bài báo là kết hợp Web3, Blockchain và Machine Learning vào chung một khung hệ thống (SWMW3).

- Các hợp đồng thông minh đã tự động hóa thành công các quy trình tài chính và theo dõi tồn kho, giúp loại bỏ cơ sở dữ liệu truyền thống, giảm thiểu lỗi do con người và tạo ra cuốn sổ cái phi tập trung an toàn.
- Việc tích hợp mô hình LSTM thông qua thư viện TensorFlow.js hoạt động mượt mà ở phía backend, trả về các kết quả dự báo thời gian thực và hiển thị trực tiếp lên bảng điều khiển (dashboard) qua chuẩn giao tiếp REST APIs.
- Xây dựng được một hệ thống quản lý kho an toàn, minh bạch, có khả năng phân tích dự đoán và tối ưu hóa quy trình hiệu quả.

## Limitations

- Không thể tích hợp toàn bộ các quy trình nghiệp vụ phức tạp của nhà kho vào chung một mô hình Học máy duy nhất. Hệ thống cần phải xây dựng và tích hợp nhiều mô hình con riêng biệt cho từng bài toán cụ thể.
- Việc áp dụng hệ thống quản lý kho phân quyền (Blockchain-based WMS) đòi hỏi doanh nghiệp phải thay đổi hoặc loại bỏ hoàn toàn hệ thống thu thập dữ liệu hiện có, gây rào cản lớn về chi phí và thời gian triển khai.
- Bài báo thiên nhiều về thiết kế kiến trúc hệ thống (System Architecture) nên phần đánh giá chuyên sâu độ tin cậy của thuật toán dự báo (thông qua các metrics) chưa được làm nổi bật.

## Relevance to our topic

Bài báo liên quan trực tiếp đến đề tài của nhóm ở phần thiết kế kiến trúc hệ thống và tích hợp học máy. Nhóm có thể tham khảo:

- Cách tích hợp mô hình Machine Learning (huấn luyện bằng Python/TensorFlow) vào hệ thống Web qua TensorFlow.js ở backend để dự báo thời gian thực.
- Cơ chế quản lý và theo dõi tồn kho dựa trên mã vạch (barcode).
- Cách thiết kế giao diện quản trị (Dashboard, Inbound/Inventory Management) phục vụ cho hiển thị thông tin.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Kế thừa kiến trúc ReactJS + ExpressJS + TensorFlow.js nhưng lược bỏ phần Blockchain/Smart Contracts để tập trung vào các thuật toán Machine Learning.
- Thay vì dự báo thời gian giao hàng, nhóm sẽ tập trung vào dự báo nhu cầu sản phẩm (Demand Forecasting) sử dụng các thuật toán như Random Forest, XGBoost hoặc LightGBM.
- Phát triển thêm mô-đun gợi ý nhập hàng (Inventory Recommendation) bằng cách so sánh tồn kho thực tế với nhu cầu dự báo.
