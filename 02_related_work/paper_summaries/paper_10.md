# Paper 10 Summary

## Citation

Tên bài: Challenges and Strategies for Inventory Management in Small and Medium-Sized Cosmetic Enterprises: A Review

Tác giả: Arthit Kittisak

Năm: 2023

Nguồn: International Journal of Information Technology and Computer Science Applications (IJITCSA), Vol. 1, No. 2, pp. 71-77

DOI/Link: https://pdfs.semanticscholar.org/b10d/578937712f5f159907573bf37c4085dca2ae.pdf

## Problem

Bài báo giải quyết vấn đề quản lý tồn kho trong các doanh nghiệp mỹ phẩm nhỏ và vừa. Các SME trong ngành mỹ phẩm thường gặp nhu cầu biến động, vòng đời sản phẩm ngắn, thị hiếu khách hàng thay đổi nhanh và nguồn lực hạn chế.

Case X Beauty gặp các vấn đề như khó tracking inventory chính xác, replenishment không đúng thời điểm, stockout lặp lại và thiếu liên kết thông tin giữa supplier, warehouse, manufacturer và customer. Điều này làm giảm doanh thu, ảnh hưởng niềm tin khách hàng và làm doanh nghiệp kém cạnh tranh.

## Method

Bài báo sử dụng qualitative research/case review, bao gồm phân tích literature và phỏng vấn/khảo sát kinh nghiệm của industry managers. Tác giả phân tích các thách thức quản lý tồn kho của SME mỹ phẩm và đề xuất giải pháp kết hợp Supply Chain Management (SCM) với Data Analytics.

Framework đề xuất gồm inventory management application kết nối database, barcode tagging, dashboard visualization và supplier access. Hệ thống theo dõi raw materials, finished products, sales, inventory movements và tự động cập nhật tồn kho khi sản xuất/bán hàng.

## Dataset

Bài báo không sử dụng dataset định lượng public. Dữ liệu nghiên cứu là thông tin định tính từ literature review, phân tích case X Beauty và input từ industry managers.

Các loại dữ liệu mà framework đề xuất cần quản lý gồm:

- Raw material inventory.
- Finished product inventory.
- Sales/order data.
- Supplier information.
- Inventory movement từ sourcing, warehousing, manufacturing đến distribution.

## Evaluation

Bài báo không đánh giá bằng metric dự báo như MAE, RMSE hoặc MAPE. Thay vào đó, bài báo đánh giá theo hướng định tính:

- Xác định inventory management challenges.
- Phân tích feasibility của SCM và data analytics.
- Đề xuất workflow cho inventory tracking và replenishment.
- Đánh giá lợi ích tiềm năng của dashboard, barcode và supplier alert.

Một điểm cụ thể trong framework là hệ thống cảnh báo supplier khi inventory xuống dưới threshold 20%.

## Results

Bài báo xác định các thách thức chính của SME mỹ phẩm:

- Inaccurate demand forecasting.
- Inadequate storage facilities.
- Inefficient inventory control systems.
- Disorganized documentation.
- Stockout và replenishment chậm.
- Thiếu IT infrastructure và thiếu nhân lực có kỹ năng.

Giải pháp đề xuất là kết hợp SCM và data analytics. Inventory management application trở thành nền tảng trung tâm cho stakeholders trong supply chain. Dashboard bằng Power BI hoặc Tableau giúp trực quan hóa inventory stock movements, product sales, company profits và KPI như current sales/current inventory. Supplier alert giúp đặt hàng sớm hơn và giảm stockout.

## Limitations

Một số hạn chế của bài báo:

- Không có thử nghiệm định lượng hoặc prototype đã triển khai.
- Chỉ tập trung vào case X Beauty và SME mỹ phẩm, nên tính khái quát còn hạn chế.
- Không sử dụng ML model cho demand forecasting, chỉ đề xuất data analytics/dashboard.
- Chưa đánh giá chi phí, thời gian triển khai hoặc ROI của hệ thống.
- Chưa có metric đo hiệu quả như stockout reduction, inventory turnover hoặc service level.

## Relevance to our topic

Bài báo liên quan đến đề tài nhóm ở góc độ nghiệp vụ và thiết kế hệ thống. Các điểm có thể tham khảo:

- SME thường thiếu dữ liệu, thiếu IT infrastructure và dễ bị stockout.
- Cần hệ thống inventory tracking thay vì spreadsheet/thủ công.
- Dashboard giúp manager ra quyết định nhanh hơn.
- Supplier alert và threshold-based replenishment là chức năng quan trọng.
- Barcode/database có thể là bước đầu trước khi áp dụng ML forecasting.

## Possible improvement

Nhóm có thể cải tiến bằng cách:

- Bổ sung ML demand forecasting vào framework SCM + Data Analytics.
- Thay threshold cố định 20% bằng reorder point hoặc safety stock tính theo demand forecast và lead time.
- Xây dựng prototype dashboard hiển thị current stock, predicted demand và recommended restock.
- Đánh giá bằng stockout rate, overstock rate, inventory turnover và forecasting metrics.
- Mở rộng từ mỹ phẩm sang warehouse/retail nhiều nhóm sản phẩm.
