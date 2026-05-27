# Weekly Report - Week 02

## Group Information

- Class: SE2037
- Group: Group 05
- Leader: Nguyen Cong Truong An - SE201020
- Members:
  - Nguyen Cong Truong An - SE201020
  - Nguyen Thach Ngon - SE201022
  - Tran Ho Phuc Duc - SE201538
  - Dang Tuan Kiet - SE201559
  - Pham Van Duc Duy - SE194521

## Tasks Completed This Week

| Member | Task | Result |
|---|---|---|
| Nguyen Cong Truong An | Tổng hợp và đề xuất bộ từ khóa tìm kiếm (Search Keywords) cho Literature Review, tạo file `search_keywords.md`. Dọn dẹp và chuẩn hóa định dạng danh sách bài báo trong `paper_list.md`. Quản lý các nhánh Git nhóm và merge Pull Request. | Hoàn thành file `search_keywords.md`, tối ưu hóa `paper_list.md` và thực hiện các commit liên quan lên Git. |
| Nguyen Thach Ngon | Sử dụng nhóm từ khóa 1 (Core Papers) tìm kiếm trên các nguồn Google Scholar, IEEE Xplore, ScienceDirect để chọn lọc các bài báo liên quan trực tiếp đến hệ thống quản lý kho kết hợp dự báo và tối ưu tồn kho. | Tìm kiếm và đóng góp 3 bài báo liên quan trực tiếp (Core Papers) vào danh sách. |
| Tran Ho Phuc Duc | Cùng tìm kiếm các bài báo liên quan trực tiếp (Core Papers). Tập trung tìm kiếm các bài báo ứng dụng Machine Learning/AI vào tự động hóa kho bãi và quản lý chuỗi cung ứng. | Tìm kiếm và đóng góp 2 bài báo liên quan trực tiếp (Core Papers) vào danh sách. |
| Dang Tuan Kiet | Sử dụng nhóm từ khóa 2 (Methodology/Model Papers) để tìm kiếm các bài báo chuyên sâu về phương pháp dự báo nhu cầu bằng Random Forest, XGBoost và các mô hình học máy dạng regression. | Tìm kiếm và đóng góp 3 bài báo về Mô hình/Phương pháp AI vào danh sách. |
| Pham Van Duc Duy | Sử dụng nhóm từ khóa 3 (Domain Papers) để tìm kiếm các tài liệu, nghiên cứu về nghiệp vụ quản lý kho truyền thống (ROP, Safety Stock, EOQ) và các thách thức thực tế tại các doanh nghiệp vừa và nhỏ (SMEs). | Tìm kiếm và đóng góp 2 bài báo về Lĩnh vực ứng dụng (Domain Papers) vào danh sách. |

## Git Commits

| Commit ID | Message | Author |
|---|---|---|
| 7056f6c | Merge pull request NCKH-LongT#24 from truongandiscovery/SE2037_G05 | truongandiscovery |
| 8dfe2d2 | docs: clean up paper list descriptions | truongandiscovery |
| efc12a4 | Merge branch 'SE2037_G05' of github.com:truongandiscovery/NCKH-SWRLocal into SE2037_G05 | truongandiscovery |
| d63b1a9 | docs: add week 1 report and paper list | truongandiscovery |

## Current Problems

- Đang bắt đầu quá trình đọc hiểu chuyên sâu và chuẩn bị viết tóm tắt từng bài báo (Paper Summaries), khối lượng tài liệu học thuật tiếng Anh tương đối nhiều và chuyên ngành sâu.
- Đang kiểm tra cấu trúc của các dataset công khai (Kaggle Online Retail/Superstore) xem có cần phải sinh thêm dữ liệu giả lập (simulated data) để đồng bộ với thuật toán gợi ý Restocking hay không.

## Plan for Next Week

- Phân chia thành viên trong nhóm đọc và viết tóm tắt chi tiết (Paper Summaries) cho 10 bài báo đã tìm được ở tuần 2 (mỗi thành viên phụ trách tóm tắt 2 bài báo theo template chuẩn của `README.md`).
- Tạo thư mục `02_related_work/paper_summaries/` và đẩy các file tóm tắt lên Git nhóm.
- Bắt đầu phân tích cấu trúc cột của dataset để thống nhất các Feature đầu vào phục vụ mô hình Random Forest/XGBoost.

## Questions for Instructor

- Nhóm em đã chọn lọc được 10 paper chất lượng thuộc cả 3 nhóm (5 Core, 3 Methodology, 2 Domain) như trong file `paper_list.md`. Nhờ thầy/cô xem qua và đánh giá xem hướng phân bổ tài liệu này đã đủ bao quát để làm cơ sở lý thuyết xây dựng mô hình dự báo nhu cầu tích hợp gợi ý nhập hàng chưa ạ?
