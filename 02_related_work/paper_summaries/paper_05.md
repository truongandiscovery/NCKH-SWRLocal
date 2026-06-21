# Paper 05 Summary

## Citation

Tên bài: Developing Requirements for Data Warehouse Systems with Use Cases
Tác giả: Robert M. Bruckner, Beate List, Josef Schiefer
Năm: 2001
Nguồn: AMCIS 2001 Proceedings
DOI/Link: https://aisel.aisnet.org/cgi/viewcontent.cgi?article=1505&context=amcis2001

## Problem

Bài báo giải quyết vấn đề thu thập và đặc tả yêu cầu cho các hệ thống hướng phân tích và hỗ trợ ra quyết định (như kho dữ liệu - Data Warehouse). Các phương pháp Kỹ thuật Yêu cầu truyền thống thường chỉ tối ưu cho các hệ thống giao dịch (OLTP) và không nắm bắt được các yêu cầu về thông tin phân tích đa chiều của người quản lý.

## Method

Bài báo sử dụng phương pháp phân tích lý thuyết, đề xuất quy trình kỹ thuật yêu cầu mở rộng (Methodology design) và minh họa cấu trúc tài liệu bằng các Use Case mẫu.

## Context

Bối cảnh nghiên cứu là việc xây dựng các hệ thống báo cáo quản trị, kho lưu trữ dữ liệu và các hệ thống hỗ trợ lãnh đạo doanh nghiệp ra quyết định dựa trên dữ liệu lịch sử.

## Key Findings

- Đề xuất một mô hình Use Case mở rộng (Data Warehouse Use Case) để liên kết chặt chẽ giữa hành động của tác nhân (Actor) với các yêu cầu về chỉ số (KPIs) và các chiều phân tích dữ liệu (Dimensions).
- Xác định rõ mối quan hệ giữa các Use Case giao dịch thông thường và Use Case phân tích nhằm duy trì tính nhất quán của dữ liệu.
- Định nghĩa các thuộc tính chất lượng dữ liệu (Data Quality Attributes) như tính kịp thời, độ chính xác, và khả năng truy xuất lịch sử để đưa vào tài liệu yêu cầu.

## Limitations

Do xuất bản từ năm 2001, một số công nghệ được đề cập trong bài đã lỗi thời, tuy nhiên cấu trúc tư duy về cách xây dựng Use Case để mô tả các yêu cầu phân tích số liệu vẫn giữ nguyên tính đúng đắn.

## Relevance to our topic

Bài báo hỗ trợ giải quyết **RQ2**: cung cấp phương pháp sử dụng Use Case để đặc tả chi tiết các luồng chức năng phân tích dữ liệu trong kho như: tổng hợp báo cáo nhập/xuất kho (stock-in/stock-out) và lập các chỉ số phục vụ khuyến nghị nhập hàng.
