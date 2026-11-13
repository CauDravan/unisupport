# Product Backlog

## 1. Purpose

Product Backlog là danh sách các chức năng và yêu cầu dự kiến được phát triển cho UniSupport. Tài liệu giúp xác định những nội dung cần có trong sản phẩm và mức độ ưu tiên tương đối của từng hạng mục.

Product Backlog được xây dựng dựa trên Product Goals, Product Scope và nhu cầu của các nhóm người dùng chính.

## 2. Priority Definitions

| Priority | Description |
|---|---|
| High | Chức năng quan trọng, cần được ưu tiên để đáp ứng các mục tiêu và phạm vi chính của dự án. |
| Medium | Chức năng bổ sung giá trị cho sản phẩm nhưng không phải ưu tiên cao nhất. |
| Low | Chức năng có thể xem xét thực hiện nếu còn thời gian và nguồn lực phù hợp. |

## 3. Product Backlog Items

| ID | Product Backlog Item | Description | Priority |
|---|---|---|---|
| PBI-01 | User Authentication | Cho phép người dùng đăng nhập vào hệ thống bằng tài khoản phù hợp. | High |
| PBI-02 | Student Request Submission | Cho phép Student tạo và gửi yêu cầu hỗ trợ bằng cách cung cấp Request Type, Subject, Description và tài liệu đính kèm nếu cần. Hệ thống tạo Request ID và xác nhận khi yêu cầu được tiếp nhận thành công. | High |
| PBI-03 | Request Tracking | Cho phép Student xem danh sách yêu cầu đã gửi, trạng thái hiện tại, lịch sử xử lý và nhận thông báo khi có cập nhật liên quan đến yêu cầu. | High |
| PBI-04 | Request Classification | Cho phép Staff xem xét và phân loại yêu cầu theo nhóm phù hợp. | High |
| PBI-05 | Request Assignment | Cho phép Staff phân công yêu cầu cho người hoặc bộ phận phụ trách. | High |
| PBI-06 | Request Processing | Cho phép Staff xem các yêu cầu được giao, cập nhật trạng thái, ghi nhận hoạt động xử lý và chuyển yêu cầu sang Staff hoặc Department khác khi cần thiết. | High |
| PBI-07 | Additional Information Handling | Cho phép Staff yêu cầu Student bổ sung thông tin và ghi nhận thông tin được cung cấp. | Medium |
| PBI-08 | Request Resolution & Closure | Cho phép Staff ghi nhận kết quả xử lý và hoàn tất yêu cầu. | High |
| PBI-09 | Student Feedback | Cho phép Student gửi đánh giá hoặc phản hồi sau khi yêu cầu được giải quyết. | Medium |
| PBI-10 | Management Dashboard | Cung cấp Dashboard giúp Management theo dõi số lượng yêu cầu mới, yêu cầu đang xử lý, yêu cầu quá hạn và các cảnh báo liên quan. | Medium |
| PBI-11 | Management Reporting | Cho phép Management xem báo cáo về thời gian xử lý trung bình, loại yêu cầu phổ biến, khối lượng công việc theo Department và dữ liệu Feedback của Student. | Medium |
| PBI-12 | Role-based Access Control | Kiểm soát quyền truy cập dựa trên vai trò Student, Staff và Management; hỗ trợ Management xem thông tin người dùng và quản lý vai trò theo quyền được cấp. | High |
| PBI-13 | Audit Logging & Data Access Protection | Ghi nhận các hoạt động quan trọng, người thực hiện, thời điểm và những thay đổi liên quan đến Request; hỗ trợ kiểm tra lịch sử xử lý và bảo vệ dữ liệu theo quyền truy cập. | High |

## 4. Backlog Management

- Product Backlog được sử dụng để quản lý các chức năng và yêu cầu dự kiến của UniSupport.
- Mức độ ưu tiên có thể được điều chỉnh khi có thay đổi về yêu cầu, nguồn lực hoặc phạm vi dự án.
- Các chức năng được lựa chọn triển khai cần phù hợp với Product Scope và thời gian thực hiện 15 tuần.
- GitHub Issues được sử dụng để phân chia và theo dõi các công việc cụ thể, bao gồm người phụ trách, tiến độ và trạng thái thực hiện.
- Những thay đổi đáng kể đối với Product Backlog cần được nhóm xem xét trước khi cập nhật.

## 5. Scope and Implementation Notes

Product Backlog hiện tại được xây dựng ở mức high-level để xác định các chức năng chính của prototype.

Việc triển khai tập trung vào các chức năng nằm trong Product Scope, sử dụng simulated data và không yêu cầu tích hợp đầy đủ với các hệ thống hiện có của trường.

Các chi tiết về giao diện, business rules, dữ liệu và Acceptance Criteria sẽ được mô tả trong những tài liệu liên quan.