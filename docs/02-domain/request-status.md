# Request Status

## Status

Mỗi request có một trạng thái thể hiện giai đoạn hiện tại của request trong quy trình hỗ trợ.

| Status                | Description                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| Received              | Yêu cầu đã được Student gửi thành công và được hệ thống tiếp nhận.                           |
| In Progress           | Yêu cầu đã được phân công cho Staff xử lý và đang được xử lý.                                |
| Awaiting Information  | Yêu cầu cần Student cung cấp thêm thông tin hoặc tài liệu trước khi có thể tiếp tục xử lý.   |
| Resolved              | Yêu cầu đã được Staff xử lý và giải quyết.                                                   |
| Closed                | Yêu cầu đã hoàn tất quá trình xử lý và được đóng chính thức.                                 |

## Status Flow

Quy trình xử lý request thông thường:

**Đã tiếp nhận → Đang xử lý → Chờ bổ sung thông tin → Đang xử lý → Đã hoàn thành → Đã đóng**

Request có thể chuyển từ **Chờ bổ sung thông tin** trở lại **Đang xử lý** sau khi Student cung cấp đầy đủ thông tin được yêu cầu.

## Priority

Mỗi request được gán một mức độ ưu tiên nhằm hỗ trợ Staff xác định thứ tự xử lý phù hợp.

| Priority   | Description                                                                          |
| ---------- | ------------------------------------------------------------------------------------ |
| Low        | Các yêu cầu có mức độ ảnh hưởng thấp và không cần được xử lý ngay lập tức.           |
| Medium     | Các yêu cầu thông thường cần được xử lý trong khoảng thời gian hỗ trợ dự kiến.       |
| Urgent     | Các yêu cầu có mức độ ảnh hưởng hoặc tính cấp thiết cao, cần được ưu tiên xử lý sớm. |

Priority là một thuộc tính của request và **không phải là một bước trong workflow**. Staff có thể sử dụng priority để sắp xếp, lọc và xác định thứ tự xử lý các request.
