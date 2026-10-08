# Request Model

## Request

Request là đối tượng dữ liệu trung tâm của UniSupport, dùng để lưu trữ và theo dõi một yêu cầu hỗ trợ của Student trong suốt quá trình xử lý.

## Request Attributes

| Attribute      | Description                                       |
| -------------- | ------------------------------------------------- |
| Request ID     | Mã định danh của yêu cầu.                         |
| Student ID     | Mã định danh của Student gửi yêu cầu.             |
| Request Type   | Loại hoặc phân loại của yêu cầu.                  |
| Subject        | Tiêu đề hoặc chủ đề của yêu cầu.                  |
| Description    | Nội dung chi tiết về vấn đề Student cần hỗ trợ.   |
| Attachment     | Tài liệu hoặc hình ảnh liên quan đến yêu cầu.     |
| Priority       | Mức độ ưu tiên của yêu cầu.                       |
| Department     | Bộ phận chịu trách nhiệm xử lý.                   |
| Assigned Staff | Staff được phân công xử lý.                       |
| Status         | Trạng thái hiện tại của yêu cầu.                  |
| Created Date   | Thời điểm tạo yêu cầu.                            |
| Updated Date   | Thời điểm cập nhật gần nhất.                      |
| Due Date       | Thời hạn xử lý yêu cầu.                           |
| Resolution     | Thông tin về kết quả xử lý.                       |
| Closed Date    | Thời điểm yêu cầu được đóng.                      |

## Request History

Request History lưu lại các hoạt động quan trọng trong quá trình xử lý yêu cầu, bao gồm:

* Thay đổi trạng thái.
* Cập nhật nội dung xử lý.
* Yêu cầu Student bổ sung thông tin.
* Chuyển yêu cầu giữa các Staff hoặc bộ phận.
* Hoàn tất hoặc đóng yêu cầu.

## Request Relationships

Một Request có liên quan đến:

* **Student** — người tạo yêu cầu.
* **Request Type** — loại yêu cầu.
* **Department** — bộ phận chịu trách nhiệm.
* **Assigned Staff** — Staff được phân công.
* **Request History** — lịch sử xử lý và cập nhật.
* **Attachment** — các tệp được gửi kèm yêu cầu.
* **Feedback** — phản hồi của Student sau khi yêu cầu được xử lý.
