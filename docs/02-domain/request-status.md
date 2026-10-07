# Request Status

## Status

Mỗi request có một trạng thái thể hiện giai đoạn hiện tại của request trong quy trình hỗ trợ.

| Status                | Description                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| Đã tiếp nhận          | Yêu cầu đã được sinh viên gửi thành công và được hệ thống tiếp nhận.                         |
| Đang xử lý            | Yêu cầu đã được phân công cho nhân viên xử lý và đang được xử lý.                            |
| Chờ bổ sung thông tin | Yêu cầu cần sinh viên cung cấp thêm thông tin hoặc tài liệu trước khi có thể tiếp tục xử lý. |
| Đã hoàn thành         | Yêu cầu đã được nhân viên xử lý và giải quyết.                                               |
| Đã đóng               | Yêu cầu đã hoàn tất quá trình xử lý và được đóng chính thức.                                 |

## Status Flow

Quy trình xử lý request thông thường:

**Đã tiếp nhận → Đang xử lý → Chờ bổ sung thông tin → Đang xử lý → Đã hoàn thành → Đã đóng**

Request có thể chuyển từ **Chờ bổ sung thông tin** trở lại **Đang xử lý** sau khi sinh viên cung cấp đầy đủ thông tin được yêu cầu.

## Priority

Mỗi request được gán một mức độ ưu tiên nhằm hỗ trợ nhân viên xác định thứ tự xử lý phù hợp.

| Priority   | Description                                                                          |
| ---------- | ------------------------------------------------------------------------------------ |
| Thấp       | Các yêu cầu có mức độ ảnh hưởng thấp và không cần được xử lý ngay lập tức.           |
| Trung bình | Các yêu cầu thông thường cần được xử lý trong khoảng thời gian hỗ trợ dự kiến.       |
| Khẩn cấp   | Các yêu cầu có mức độ ảnh hưởng hoặc tính cấp thiết cao, cần được ưu tiên xử lý sớm. |

Priority là một thuộc tính của request và **không phải là một bước trong workflow**. Nhân viên có thể sử dụng priority để sắp xếp, lọc và xác định thứ tự xử lý các request.
