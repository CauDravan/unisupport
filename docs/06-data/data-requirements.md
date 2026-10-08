# Data Requirements

## 1. Purpose

Tài liệu này mô tả các nhóm dữ liệu chính mà UniSupport cần quản lý để hỗ trợ các chức năng của hệ thống.

Data Requirements tập trung vào **loại dữ liệu cần có và mục đích sử dụng của dữ liệu**. Chi tiết về các thuộc tính của Request được mô tả trong `02-domain/request-model.md`, trong khi Status và Priority được mô tả trong `02-domain/request-status.md`.

## 2. User Data

User Data được sử dụng để quản lý thông tin cơ bản của người dùng và xác định vai trò của họ trong hệ thống.

Hệ thống cần quản lý thông tin của các nhóm người dùng chính:

* **Student** — người gửi và theo dõi các yêu cầu hỗ trợ.
* **Staff** — người tiếp nhận, xử lý và cập nhật các yêu cầu.
* **Management** — người theo dõi tình hình hỗ trợ và sử dụng các chức năng báo cáo.

User Data hỗ trợ việc xác định người dùng, phân quyền truy cập và liên kết người dùng với các hoạt động trong hệ thống.

## 3. Request Data

Request Data là nhóm dữ liệu trung tâm của UniSupport, được sử dụng để lưu trữ các yêu cầu hỗ trợ do Student gửi.

Request Data cần hỗ trợ việc:

* Xác định request và Student tạo request.
* Lưu nội dung và loại yêu cầu hỗ trợ.
* Xác định mức độ ưu tiên của request.
* Xác định Department và Staff chịu trách nhiệm xử lý.
* Theo dõi tình trạng xử lý của request.
* Lưu thông tin về kết quả xử lý và thời gian liên quan.

Các thuộc tính chi tiết của Request được mô tả trong `02-domain/request-model.md`.

## 4. Request History / Activity Data

Request History / Activity Data được sử dụng để ghi nhận các hoạt động quan trọng xảy ra trong quá trình xử lý request.

Dữ liệu này hỗ trợ việc theo dõi lịch sử xử lý, bao gồm:

* Thay đổi trạng thái request.
* Cập nhật nội dung xử lý.
* Yêu cầu Student bổ sung thông tin.
* Chuyển request giữa Staff hoặc Department.
* Hoàn tất hoặc đóng request.

Request History giúp Staff và Management có thể theo dõi quá trình xử lý và lịch sử thay đổi của request.

## 5. Attachment Data

Attachment Data được sử dụng để quản lý các tệp hoặc tài liệu được Student gửi kèm request.

Dữ liệu này cần hỗ trợ việc:

* Liên kết tệp với request tương ứng.
* Xác định tệp được gửi cùng request.
* Cho phép Staff sử dụng tài liệu đính kèm trong quá trình xử lý.

Attachment được xem là dữ liệu liên quan đến Request và được quản lý theo quyền truy cập của người dùng.

## 6. Feedback Data

Feedback Data được sử dụng để lưu trữ phản hồi của Student sau khi request được xử lý.

Dữ liệu này hỗ trợ:

* Ghi nhận đánh giá của Student về kết quả hỗ trợ.
* Lưu phản hồi liên quan đến request.
* Cung cấp thông tin cho Management trong việc đánh giá chất lượng dịch vụ hỗ trợ.

## 7. Data Usage

Các nhóm dữ liệu trên được sử dụng để hỗ trợ các chức năng chính của UniSupport:

| Data Group                      | Main Usage                                               |
| ------------------------------- | -------------------------------------------------------- |
| User Data                       | Xác định người dùng và vai trò trong hệ thống.           |
| Request Data                    | Tạo, xử lý và theo dõi yêu cầu hỗ trợ.                   |
| Request History / Activity Data | Theo dõi lịch sử và quá trình xử lý request.             |
| Attachment Data                 | Quản lý tài liệu được gửi kèm request.                   |
| Feedback Data                   | Ghi nhận phản hồi và hỗ trợ đánh giá chất lượng dịch vụ. |

## 8. Data Privacy

Prototype của UniSupport sử dụng dữ liệu mô phỏng thay cho dữ liệu cá nhân thực tế.

Dữ liệu cần được truy cập theo vai trò của người dùng. Student chỉ được truy cập dữ liệu liên quan đến các request của mình, trong khi Staff và Management được truy cập dữ liệu phù hợp với quyền hạn được cấp.

Chi tiết về Security & Access Control được mô tả trong module **M04 — Security and Access**.
