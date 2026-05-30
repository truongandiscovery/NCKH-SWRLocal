# Paper 02 Summary

## Citation

Tên bài: Predictive models for inventory optimization: a machine learning application for demand forecasting at a construction supplies distributor

Tác giả: Diocélio Dornela Goulart, Rodrigo Baroni de Carvalho, Mariana Almeida Henriques and Bárbara Kawany Gonçalves Nunes Carvalho

Năm: 2026

Nguồn: Future Business Journal

DOI/Link: https://doi.org/10.1186/s43093-026-00807-8

## Problem

Quản lý tồn kho là bài toán cốt lõi của các công ty phân phối, nơi những sai sót trong dự báo có thể dẫn đến dư thừa hàng (tăng chi phí lưu trữ) hoặc thiếu hụt hàng (stockouts, gây mất doanh thu). Các mô hình dự báo truyền thống thường gặp khó khăn với dữ liệu phức tạp, có tính mùa vụ và nhiều biến động. Bài báo tập trung giải quyết thách thức của các doanh nghiệp vừa và nhỏ (SMEs), cụ thể là Casa Cardão (một nhà phân phối vật liệu xây dựng tại Brazil), nơi có nguồn lực CNTT hạn chế và thiếu hụt đội ngũ chuyên gia về Khoa học Dữ liệu (Data Science) hay Trí tuệ nhân tạo (AI).

## Method

Bài báo xây dựng hệ thống dự báo bằng cách sử dụng nền tảng học máy tự động trên đám mây (Cloud-based AutoML), cụ thể là Amazon Forecast và Amazon SageMaker Canvas. Hệ thống hoạt động theo kiến trúc sau:

- Trích xuất dữ liệu (ETL): Dùng SageMaker Data Wrangler để xử lý dữ liệu và đưa vào Data Lake (Amazon S3).
- Huấn luyện mô hình: Sử dụng nền tảng đám mây để tự động đánh giá và chọn thuật toán tốt nhất, trong đó DeepAR+ (dựa trên mạng nơ-ron hồi quy - RNN và mô hình LSTM của Amazon) mang lại hiệu quả cao nhất.
- Giao diện trực quan: Xây dựng một Dashboard tương tác bằng React, tích hợp AI tạo sinh (GPT) để giải thích phương pháp và cung cấp các kịch bản dự báo (Lạc quan - P80, Trung lập - P50, Bi quan - P35) hỗ trợ người quản lý.

## Dataset

Nghiên cứu sử dụng dữ liệu thực tế từ hệ thống ERP và CRM của công ty phân phối (dữ liệu nội bộ), kết hợp với dữ liệu ngoại vi (thời tiết, lịch nghỉ lễ, chỉ số kinh tế vĩ mô). Đối với một mã sản phẩm thử nghiệm (ống thoát nước Amanco), dữ liệu bao gồm 16 tháng ghi nhận hàng ngày (tháng 7/2023 - tháng 11/2024) với 11.074 lượt quan sát. Tập dữ liệu được chia theo tỷ lệ 80% để huấn luyện (train) và 20% để kiểm thử (backtesting), với khung thời gian dự báo là 60 ngày.

## Evaluation

Bài báo đánh giá hiệu suất mô hình thông qua các chỉ số: RMSE (Root Mean Squared Error), MAPE (Mean Absolute Percentage Error), MASE (Mean Absolute Scaled Error), và WAPE (Weighted Absolute Percentage Error). Trong đó, WAPE được chọn làm chỉ số đo lường chính vì nó phản ánh sai số dựa trên trọng số khối lượng bán hàng, ít bị độ lệch bởi các mặt hàng có doanh số quá thấp.

## Results

Mô hình DeepAR+ đạt được sai số WAPE xấp xỉ 0.69% trong giai đoạn đánh giá. Bài báo đã chứng minh tính khả thi trong việc triển khai một hệ thống dự báo nhu cầu đầu-cuối (end-to-end) cho một SME trước đây chỉ quen với các báo cáo dữ liệu mô tả (descriptive analytics). Giá trị đóng góp lớn nhất không nằm ở tính mới của thuật toán, mà là cung cấp một "bản thiết kế" kiến trúc (blueprint) giúp các SME có thể ứng dụng nền tảng AutoML một cách thực tế mà không cần phải xây dựng một đội ngũ Data Science chuyên biệt.

## Limitations

- Chỉ số tổng hợp WAPE có thể bị chi phối bởi các sản phẩm có khối lượng bán ra cao, làm che lấp sai số ở các sản phẩm bán chậm.
- Nền tảng AWS AutoML hoạt động như một "hộp đen", thiếu sự đối chiếu trực tiếp với các mô hình cơ sở (naïve baselines) và thiếu tính minh bạch trong việc tinh chỉnh các siêu tham số (hyperparameters).
- Chưa giải quyết được bài toán thiếu dữ liệu (cold-start problem) đối với các sản phẩm mới ra mắt chưa có lịch sử bán hàng.
- Phụ thuộc vào nền tảng đám mây dẫn đến rủi ro lệ thuộc nhà cung cấp (vendor lock-in) và phát sinh chi phí vận hành hàng tháng.

## Relevance to our topic

Bài báo liên quan trực tiếp đến đề tài của nhóm ở phần thiết kế kiến trúc hệ thống và xây dựng dashboard. Nhóm có thể học cách:

- Thiết kế kiến trúc hệ thống hoàn chỉnh: Từ trích xuất dữ liệu (ETL), lưu trữ (Data Lake), huấn luyện tự động (AutoML) đến xây dựng Dashboard.
- Thiết kế giao diện kết hợp các kịch bản tồn kho (lạc quan, trung lập, bi quan) để đưa ra gợi ý nhập hàng hỗ trợ nhà quản lý.
- Xây dựng hệ thống có tính ứng dụng cao hướng tới doanh nghiệp vừa và nhỏ (SMEs) có nguồn lực kỹ thuật hạn chế.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Sử dụng các mô hình mã nguồn mở (như Prophet, LSTM hoặc Random Forest) thay vì phụ thuộc vào giải pháp đám mây thương mại như AWS Canvas để tăng tính minh bạch và dễ dàng so sánh hiệu suất với các mô hình cơ sở.
- Thiết kế cơ chế dự báo riêng biệt để giải quyết bài toán thiếu dữ liệu (cold-start) khi có mặt hàng hoàn toàn mới được nhập kho.
- Phát triển thêm mô-đun phân tích đề xuất để tính toán lượng đặt hàng tối ưu (order quantities) và tồn kho an toàn (safety stocks) nhằm đưa ra đề xuất nhập hàng trực tiếp.
