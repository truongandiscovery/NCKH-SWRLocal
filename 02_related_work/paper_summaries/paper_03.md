# Paper 03 Summary

## Citation

Tên bài: A Framework for Modelling Software Requirements
Tác giả: Dhirendra Pandey, Ugrasen Suman, A. K. Ramani
Năm: 2011
Nguồn: International Journal of Computer Science Issues (IJCSI), Vol. 8, Issue 3, No. 1, May 2011
DOI/Link: https://www.researchgate.net/profile/Ugrasen-Suman/publication/266000842_A_Framework_for_Modelling_Software_Requirements/links/55094f260cf2d7a2812c6e71/A-Framework-for-Modelling-Software-Requirements.pdf

## Problem

Bài báo giải quyết vấn đề đặc tả yêu cầu phần mềm chủ yếu dựa vào văn bản thuần túy (textual specifications), vốn mơ hồ, khó hiểu đối với stakeholder phi kỹ thuật và dễ dẫn đến hiểu lầm giữa người dùng và đội phát triển. Không có một khung thống nhất nào kết hợp đầy đủ các công cụ mô hình hóa khác nhau để bao phủ toàn bộ vòng đời phát triển hệ thống từ giai đoạn thu thập yêu cầu đến đặc tả chức năng và giao diện.

## Method

Bài báo đề xuất một **Software Requirements Modelling Framework** — khung tích hợp nhiều công cụ mô hình hóa trực quan thay thế cho tài liệu đặc tả văn bản. Các thành phần của khung bao gồm:

- **Semantic Map**: mô hình hóa các khái niệm nghiệp vụ và mối quan hệ giữa chúng.
- **Business Object Lifecycle**: biểu diễn vòng đời của từng đối tượng nghiệp vụ (ví dụ: đơn hàng, sản phẩm, phiếu nhập kho).
- **Business Process Model**: mô hình hóa các quy trình nghiệp vụ và luồng công việc.
- **Business Rules**: mô tả các ràng buộc và quy tắc nghiệp vụ.
- **System Context Diagram**: xác định ranh giới hệ thống và tương tác với môi trường bên ngoài.
- **Use Cases và Scenarios**: đặc tả các ca sử dụng chính và luồng thực thi.
- **Constraints**: xác định các ràng buộc phi chức năng.
- **User Interface Prototypes**: xây dựng bản mẫu giao diện người dùng để trực quan hóa yêu cầu.

Toàn bộ khung được áp dụng thực tế qua **Case Study: Inventory Management System**, trong đó các mô hình được minh họa cụ thể qua quy trình nhập hàng, trả hàng và kiểm soát tồn kho.

## Context

Nghiên cứu được thực hiện trong bối cảnh học thuật, tập trung vào giai đoạn Requirements Engineering trong Software Development Life Cycle (SDLC). Hệ thống quản lý kho (Inventory Management System) được chọn làm ví dụ minh họa xuyên suốt vì tính phổ biến và đủ độ phức tạp để thể hiện toàn bộ các thành phần của khung. Bài báo hướng đến đối tượng là kỹ sư phần mềm và business analyst cần công cụ mô hình hóa có hệ thống ngay từ đầu chu kỳ phát triển.

## Key Findings

- Mô hình hóa trực quan bằng sơ đồ (pictorial modeling) hiệu quả hơn đặc tả văn bản thuần túy trong việc truyền đạt yêu cầu đến stakeholder phi kỹ thuật.
- Kết hợp **Use Case Diagram** và **UI Prototype** giúp stakeholder hình dung và xác nhận yêu cầu chính xác hơn, giảm thiểu rủi ro hiểu lầm trong giai đoạn phân tích.
- **Business Object Lifecycle** giúp phát hiện sớm các trạng thái và chuyển tiếp còn thiếu hoặc mâu thuẫn trong quy trình nghiệp vụ.
- Tất cả các thành phần của khung đều có thể ánh xạ tương ứng sang các phần tử UML chuẩn, giúp chuyển đổi sang giai đoạn thiết kế và triển khai một cách có cấu trúc.
- Áp dụng khung vào hệ thống quản lý kho cho thấy khả năng phát hiện các yêu cầu thiếu sót (ví dụ: điều kiện trả hàng, trạng thái tồn kho âm) ngay trong giai đoạn đầu mà tài liệu văn bản thường bỏ qua.

## Limitations

- Khung được đề xuất ở mức học thuật và chưa được kiểm chứng trong các dự án công nghiệp quy mô lớn với nhiều stakeholder và yêu cầu phức tạp.
- Việc xây dựng đồng thời nhiều loại mô hình (semantic map, lifecycle, use case, prototype) đòi hỏi đầu tư thời gian và kỹ năng công cụ đáng kể, có thể không khả thi với các nhóm nhỏ hoặc dự án ngắn hạn.
- Khung chưa đề cập đến cơ chế quản lý thay đổi yêu cầu (requirements change management) và traceability giữa các mô hình khi yêu cầu thay đổi trong quá trình phát triển.

## Relevance to our topic

Bài báo liên quan trực tiếp đến **RQ2** và **RQ3** của nhóm. Đối với **RQ2** (đặc tả yêu cầu chức năng): khung đề xuất cung cấp phương pháp mô hình hóa hệ thống quản lý kho bằng Use Case Diagram và Business Process Model — giúp nhóm có cơ sở phương pháp luận để đặc tả các chức năng cốt lõi như quản lý nhập/xuất kho, cảnh báo tồn kho và xử lý đơn hàng. Đối với **RQ3** (giao diện và trải nghiệm người dùng): kỹ thuật UI Prototype trong khung cung cấp hướng tiếp cận trực quan hóa yêu cầu giao diện cho cả quản lý kho lẫn nhân viên vận hành, phù hợp với mục tiêu thiết kế hệ thống dễ sử dụng của nhóm.
