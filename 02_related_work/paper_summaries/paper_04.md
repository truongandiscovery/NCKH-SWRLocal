# Paper 04 Summary

## Citation

Tên bài: Demand Driven Material Requirements Planning: An Inventory Optimization Model
Tác giả: Dr. Muragesh Math, Dr. Gopinath Duggi, B. S. Biradar
Năm: 2024
Nguồn: International Journal of Agricultural and Statistical Sciences, Vol. 20, No. 1, pp. 105–112
DOI/Link: https://www.researchgate.net/profile/Dr-Math/publication/381343552_Demand_Driven_Material_Requirements_Planning_An_Inventory_Optimization_Model/links/66aba592299c327096a2fccb/Demand-Driven-Material-Requirements-Planning-An-Inventory-Optimization-Model.pdf

## Problem

Bài báo giải quyết vấn đề xác định mức tồn kho an toàn (safety stock) trong các hệ thống sản xuất và phân phối đa cấp có tính ngẫu nhiên (stochastic multi-state systems). Hệ thống MRP (Material Requirements Planning) truyền thống phụ thuộc vào dự báo cầu tĩnh và thường xuyên không chính xác, dẫn đến hai hậu quả chính: (1) tồn kho dư thừa làm tăng chi phí lưu kho và đóng băng vốn, hoặc (2) thiếu hàng gây gián đoạn chuỗi cung ứng và mất khách hàng. Vấn đề cốt lõi là chưa có công thức toán học nhất quán để tính safety stock trong bối cảnh DDMRP khi cầu tuân theo phân phối xác suất chuẩn (normal probability distribution).

## Method

Bài báo đề xuất một **mô hình tối ưu hóa tồn kho mới** trong khuôn khổ **Demand Driven Material Requirements Planning (DDMRP)**, bao gồm:

- **Công thức tính safety stock mới**: được xây dựng dựa trên lý thuyết xác suất và phân phối chuẩn, đảm bảo tính nhất quán toán học khi áp dụng vào mô hình đa cấp ngẫu nhiên.
- **Hệ thống buffer zones 3 vùng**: phân loại mức tồn kho thành ba vùng chiến lược:
  - **Vùng Đỏ (Red Zone)**: mức tối thiểu cần duy trì để không bị đứt hàng, kích hoạt lệnh đặt hàng khẩn cấp.
  - **Vùng Vàng (Yellow Zone)**: mức tồn kho bình thường, kích hoạt đặt hàng theo chu kỳ thông thường.
  - **Vùng Xanh (Green Zone)**: mức tồn kho mục tiêu, cho thấy hệ thống đang vận hành tối ưu.
- **Validation qua Case Study**: mô hình được kiểm chứng trên dữ liệu thực tế từ một công ty FMCG (Fast-Moving Consumer Goods) lớn tại Đông Nam Á, với mục tiêu đạt tỷ lệ đáp ứng đơn hàng (fill rate) 99%.

## Context

Nghiên cứu được thực hiện trong bối cảnh quản lý chuỗi cung ứng hiện đại, cụ thể là hệ thống phân phối hàng tiêu dùng nhanh (FMCG) tại Đông Nam Á — một môi trường đặc trưng bởi nhu cầu biến động mạnh theo mùa vụ, nhiều cấp phân phối (nhà sản xuất → nhà phân phối → bán lẻ) và yêu cầu dịch vụ khách hàng cao. Đây là bối cảnh điển hình của các bài toán tồn kho phức tạp mà MRP truyền thống không xử lý được hiệu quả.

## Key Findings

- Công thức tính safety stock được đề xuất duy trì tính nhất quán toán học khi áp dụng với phân phối xác suất chuẩn trong hệ thống đa cấp, khắc phục được điểm yếu của các phương pháp DDMRP hiện có.
- Mô hình buffer zones 3 màu (Red/Yellow/Green) cho phép hệ thống **tự động phân loại trạng thái tồn kho** và kích hoạt hành động phù hợp (đặt hàng khẩn/thường/chờ) mà không cần can thiệp thủ công liên tục.
- Áp dụng vào công ty FMCG Đông Nam Á cho thấy mô hình DDMRP cải thiện đáng kể khả năng duy trì fill rate 99%, giảm tình trạng stockout so với cách tính safety stock cũ dựa trên dự báo tĩnh.
- Mức reorder point được xác định động theo biến động cầu thực tế (demand variability) thay vì một ngưỡng cố định, giúp hệ thống thích ứng tốt hơn với thị trường không ổn định.
- Kết quả cho thấy phương pháp này đặc biệt hiệu quả ở cấp nhà phân phối (distributor level) — nơi tồn kho thường bị overstock do lo ngại thiếu hàng từ cấp trên.

## Limitations

- Mô hình đòi hỏi dữ liệu lịch sử tiêu thụ đủ dài và chất lượng cao để ước lượng chính xác các tham số phân phối xác suất (trung bình, độ lệch chuẩn của cầu). Doanh nghiệp nhỏ hoặc mới thành lập thiếu dữ liệu lịch sử sẽ khó áp dụng ngay.
- Nghiên cứu được validate trên một công ty FMCG đơn lẻ tại Đông Nam Á — kết quả có thể không hoàn toàn tổng quát cho các ngành khác (ví dụ: kho linh kiện kỹ thuật, kho dược phẩm) nơi cấu trúc cầu và ràng buộc tồn kho khác biệt.
- Khung DDMRP yêu cầu thay đổi quy trình vận hành và đào tạo nhân viên — chi phí chuyển đổi từ MRP truyền thống có thể là rào cản đáng kể cho doanh nghiệp vừa và nhỏ.

## Relevance to our topic

Bài báo liên quan trực tiếp đến **RQ2** của nhóm về đặc tả yêu cầu tối ưu hóa tồn kho. Cụ thể, mô hình buffer zones 3 màu (Red/Yellow/Green) và công thức xác định reorder point động cung cấp **nền tảng lý thuyết và toán học** để nhóm đặc tả các yêu cầu chức năng cốt lõi của hệ thống: (1) logic cảnh báo tồn kho theo ngưỡng động, (2) thuật toán tự động gợi ý số lượng và thời điểm nhập hàng, (3) phân loại trạng thái kho theo vùng màu để hiển thị dashboard trực quan. Đây là bài báo nền tảng để nhóm xây dựng phần **Functional Requirements** liên quan đến module cảnh báo và đề xuất nhập hàng trong hệ thống quản lý kho thông minh.
