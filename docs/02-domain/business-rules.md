# Business Rules

## Request Status

* Mỗi yêu cầu chỉ có một trạng thái hiện tại.
* Yêu cầu có thể chuyển từ **"Chờ bổ sung thông tin"** trở lại **"Đang xử lý"** sau khi sinh viên cung cấp đầy đủ thông tin được yêu cầu.

## Request Priority

* Mỗi yêu cầu được gán một mức độ ưu tiên.
* Mức độ ưu tiên được xác định dựa trên mức độ ảnh hưởng và tính cấp thiết của yêu cầu.
* Mức độ ưu tiên là một thuộc tính của yêu cầu và không phải là một bước trong quy trình xử lý.

## Request History

* Các thay đổi về trạng thái và mức độ ưu tiên phải được ghi nhận trong lịch sử yêu cầu.
* Các hoạt động xử lý cần được ghi nhận để phục vụ việc theo dõi và giám sát.

## Additional Information

* Khi yêu cầu chuyển sang trạng thái **"Chờ bổ sung thông tin"**, sinh viên cần được thông báo để cung cấp thông tin cần thiết.
