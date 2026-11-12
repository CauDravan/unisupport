# M04 – Security & Access

## Purpose

Module hỗ trợ **kiểm soát quyền truy cập và bảo vệ các chức năng của hệ thống** dựa trên vai trò của người sử dụng. Module này được áp dụng xuyên suốt các module khác thay vì hoạt động như một giao diện độc lập.

## Users

* Student
* Staff
* Management

## Main capabilities

### 1. Role-Based Access Control

Hệ thống phân quyền người sử dụng dựa trên vai trò được cấp.

Mỗi vai trò chỉ được phép truy cập và thực hiện các chức năng phù hợp với quyền của mình:

* **Student:** gửi yêu cầu, xem các yêu cầu của mình và cung cấp thêm thông tin hoặc phản hồi.
* **Staff:** xem các yêu cầu được phân công, phân loại, phân công hoặc chuyển yêu cầu, cập nhật trạng thái và hoàn tất xử lý.
* **Management:** truy cập dashboard, xem báo cáo và quản lý người dùng hoặc vai trò.

### 2. Access Restriction

Hệ thống phải ngăn người sử dụng truy cập các chức năng không thuộc quyền của mình.

Ví dụ:

* Student không được truy cập các chức năng xử lý yêu cầu dành cho Staff.
* Staff không được truy cập các chức năng quản lý dành cho Management nếu không được cấp quyền.
* Management có thể truy cập các chức năng quản lý theo quyền được cấp.

### 3. Activity Logging

Hệ thống ghi nhận các hoạt động cần thiết liên quan đến quá trình sử dụng và xử lý yêu cầu.

Thông tin được ghi nhận có thể bao gồm:

* Người thực hiện thao tác.
* Thao tác được thực hiện.
* Thời điểm thực hiện.
* Thay đổi liên quan đến yêu cầu.

Các thông tin này được sử dụng để theo dõi lịch sử xử lý và hỗ trợ việc kiểm tra khi cần thiết.

### 4. User and Role Management

Management có thể quản lý người dùng và vai trò trong hệ thống theo quyền được cấp.

Chức năng này hỗ trợ:

* Xem thông tin người dùng.
* Xác định vai trò của người dùng.
* Cập nhật vai trò khi cần thiết.

## Related Functional Requirements

* Role Permission Matrix
* Security & Access Control
* Activity Logging
