# Paper 09 Summary

## Citation

Tên bài: Comprehensive Review of Improvement in Inventory Management Methods through Digitalization: Traditional Practices and Emerging Trends

Tác giả: Sara Rezaeinavaei, Sharfuddin Khan

Năm: 2025

Nguồn: Proceedings of the 2nd World Congress on Industrial Engineering and Operations Management, Windsor, Canada, October 14-16, 2025

DOI/Link: https://doi.org/10.46254/WC02.20250174

## Problem

Bài báo giải quyết vấn đề các phương pháp quản lý tồn kho truyền thống như EOQ, JIT, MRP, ROP và ABC analysis vẫn hữu ích trong môi trường ổn định nhưng không còn đủ linh hoạt cho chuỗi cung ứng hiện đại. Nhu cầu hiện nay biến động nhanh, lead time không chắc chắn, doanh nghiệp cần real-time visibility, traceability và khả năng phản ứng nhanh hơn.

Trong khi đó, công nghệ số như AI, ML, IoT, RFID, blockchain, ERP và Big Data analytics có thể cải thiện dự báo, theo dõi tồn kho và tự động hóa, nhưng cũng gặp rào cản về chi phí, kỹ thuật, tích hợp hệ thống cũ và thiếu nhân lực. Bài báo tập trung vào khoảng trống: thiếu một khung so sánh và kết hợp giữa traditional inventory methods và digital inventory methods.

## Method

Bài báo sử dụng systematic literature review kết hợp comparative analysis. Tác giả tổng hợp các nghiên cứu về:

- Traditional methods: EOQ, JIT, MRP, ROP, ABC analysis.
- Digital/emerging methods: AI, ML, IoT, RFID, blockchain, ERP, Big Data analytics.

Sau đó, bài báo so sánh các phương pháp theo tiêu chí như effectiveness, adaptability, scalability, integration complexity và traceability. Từ đó, tác giả đề xuất một hybrid inventory management framework kết hợp sự ổn định, đơn giản và chi phí thấp của phương pháp truyền thống với khả năng real-time, automation và predictive analytics của công nghệ số.

## Dataset

Bài báo không sử dụng dataset thực nghiệm cụ thể vì đây là review paper. Dữ liệu nghiên cứu là các tài liệu học thuật và nguồn ngành liên quan đến inventory management, supply chain digitalization và inventory optimization.

Nguồn phân tích bao gồm nghiên cứu về EOQ, JIT, MRP, ROP, ABC, AI/ML, IoT, RFID, blockchain, ERP và Big Data analytics trong các bối cảnh như manufacturing, retail, logistics, healthcare, agriculture và SMEs.

## Evaluation

Bài báo không đánh giá bằng MAE, RMSE hay MAPE. Thay vào đó, các phương pháp được so sánh bằng tiêu chí định tính:

- Effectiveness: khả năng tối ưu tồn kho và giảm chi phí.
- Adaptability: khả năng thích nghi với biến động nhu cầu và supply chain disruption.
- Scalability: khả năng mở rộng.
- Implementation complexity: độ khó triển khai.
- Traceability/transparency: khả năng theo dõi, minh bạch và truy xuất nguồn gốc.
- Fit by context: mức phù hợp với môi trường ổn định, SME hoặc chuỗi cung ứng số hóa.

## Results

Kết quả chính:

- Traditional methods vẫn có giá trị vì đơn giản, dễ hiểu, chi phí thấp và phù hợp với môi trường ổn định.
- Hạn chế của traditional methods là giả định demand/lead time ổn định, khó xử lý disruption và thiếu real-time responsiveness.
- Digital technologies cải thiện predictive capability, real-time monitoring, automation, traceability và transparency.
- Rào cản của digitalization gồm chi phí triển khai, integration với legacy systems, data privacy, cybersecurity và thiếu kỹ năng.
- Hybrid approach là hướng phù hợp, đặc biệt cho SMEs cần chuyển đổi số từng bước.

## Limitations

Một số hạn chế của bài báo:

- Đây là review paper, chưa có thực nghiệm trên dataset cụ thể.
- Hybrid framework còn ở mức khái niệm, chưa có kiến trúc kỹ thuật chi tiết.
- Chưa có kết quả định lượng về giảm stockout, giảm overstock hoặc ROI.
- Chưa kiểm chứng framework bằng case study trong doanh nghiệp thực tế.
- Một số công nghệ được phân tích ở mức tổng quan, chưa đi sâu vào thuật toán hoặc pipeline triển khai.

## Relevance to our topic

Bài báo rất phù hợp để làm nền tảng lý thuyết cho đề tài nhóm. Nhóm có thể dùng bài này để giải thích vì sao hệ thống quản lý kho nên kết hợp:

- Phương pháp truyền thống như ROP, safety stock, ABC analysis.
- ML forecasting để dự báo nhu cầu.
- Dashboard và real-time inventory tracking.
- Lộ trình chuyển đổi số phù hợp với SMEs.

## Possible improvement

Nhóm có thể phát triển từ paper này bằng cách:

- Xây dựng prototype hybrid cụ thể cho warehouse management.
- Dùng ML để dự báo demand, sau đó dùng ROP/safety stock để gợi ý nhập hàng.
- Đánh giá bằng cả forecasting metrics và inventory KPIs.
- Thiết kế dashboard thể hiện predicted demand, current stock, reorder point và recommended restock quantity.
- Mô phỏng barcode/RFID ở mức đơn giản để cập nhật nhập/xuất kho theo thời gian thực.
