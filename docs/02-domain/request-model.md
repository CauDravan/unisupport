# Request Model

## Request

Request là đối tượng dữ liệu trung tâm của UniSupport, dùng để lưu trữ và theo dõi một yêu cầu hỗ trợ của Student trong suốt quá trình xử lý.

## Request Attributes

| Attribute | Description |
|---|---|
| Request ID | Mã định danh duy nhất của yêu cầu. |
| Student ID | Mã định danh của Student gửi yêu cầu. |
| Request Type | Loại yêu cầu hỗ trợ. |
| Subject | Tiêu đề hoặc chủ đề của yêu cầu. |
| Description | Nội dung chi tiết về vấn đề Student cần hỗ trợ. |
| Attachments | Các tài liệu hoặc hình ảnh được gửi kèm yêu cầu. |
| Priority | Mức độ ưu tiên của yêu cầu. |
| Department | Bộ phận chịu trách nhiệm xử lý yêu cầu hiện tại. |
| Assigned Staff | Staff hiện được phân công xử lý yêu cầu. |
| Status | Trạng thái hiện tại của yêu cầu. |
| Created Date | Thời điểm tạo yêu cầu. |
| Updated Date | Thời điểm cập nhật gần nhất. |
| Due Date | Thời hạn xử lý yêu cầu. |
| Resolution | Thông tin về kết quả xử lý yêu cầu. |
| Closed Date | Thời điểm yêu cầu được đóng. |

**Note:** Department và Assigned Staff có thể chưa được xác định tại thời điểm Request được tạo hoặc trong quá trình chờ phân công.

## Request History

Request History lưu lại các hoạt động và thay đổi quan trọng trong quá trình xử lý yêu cầu, bao gồm:

- Thay đổi trạng thái.
- Thay đổi mức độ ưu tiên.
- Thay đổi Department hoặc Assigned Staff.
- Cập nhật nội dung xử lý.
- Yêu cầu Student bổ sung thông tin.
- Chuyển yêu cầu giữa các Staff hoặc bộ phận.
- Hoàn tất hoặc đóng yêu cầu.

Mỗi bản ghi lịch sử cần lưu thông tin về người thực hiện, loại hoạt động, nội dung thay đổi và thời điểm thực hiện.

## Request Relationships

Một Request có liên quan đến các đối tượng sau:

- **Student:** Một Student có thể tạo nhiều Request. Mỗi Request thuộc về một Student.
- **Request Type:** Một Request thuộc một Request Type. Một Request Type có thể được sử dụng bởi nhiều Request.
- **Department:** Một Request có thể được giao cho một Department tại một thời điểm. Một Department có thể tiếp nhận nhiều Request.
- **Assigned Staff:** Một Request có thể được phân công cho một Staff tại một thời điểm hoặc chưa có Staff được phân công. Một Staff có thể xử lý nhiều Request.
- **Request History:** Một Request có thể có nhiều bản ghi Request History.
- **Attachments:** Một Request có thể có nhiều tệp đính kèm.
- **Feedback:** Một Request có thể có Feedback từ Student sau khi được xử lý.