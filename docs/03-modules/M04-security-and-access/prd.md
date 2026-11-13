# M04 – Security & Access

## Purpose

## Purpose

Module hỗ trợ kiểm soát quyền truy cập và bảo vệ dữ liệu trong hệ thống UniSupport dựa trên vai trò của người sử dụng. Module đảm bảo Student, Staff và Management chỉ có thể truy cập các chức năng và dữ liệu thuộc phạm vi quyền được cấp.

Ngoài ra, Module hỗ trợ ghi nhận các hoạt động quan trọng, bảo vệ thông tin sinh viên và tài liệu đính kèm, đồng thời xem xét yêu cầu về thời gian lưu trữ và xử lý dữ liệu nhạy cảm.

Module được áp dụng xuyên suốt các module khác thay vì hoạt động như một giao diện độc lập.

## Users

### 1. Student
- Truy cập chức năng dành cho sinh viên.
- Chỉ xem Request và Attachment thuộc tài khoản của mình.
- Cung cấp thông tin bổ sung và gửi Feedback theo quyền được cấp.

### 2. Staff
- Truy cập Request thuộc phạm vi được phân công hoặc quyền được cấp.
- Thực hiện các thao tác xử lý Request theo trách nhiệm.
- Không truy cập dữ liệu hoặc chức năng ngoài quyền hạn.

### 3. Management
- Truy cập Dashboard và báo cáo theo quyền được cấp.
- Theo dõi hoạt động và thông tin quản lý phù hợp với quyền hạn.
- Các thao tác quản lý người dùng và Role cần tuân theo phạm vi được xác nhận trong dự án.

## Main capabilities

### 1. Role-Based Access Control

Hệ thống kiểm soát quyền truy cập dựa trên Role của người sử dụng. Mỗi người dùng phải được xác định vai trò và chỉ được phép thực hiện các chức năng thuộc phạm vi quyền được cấp.

Các quyền truy cập chính bao gồm:

- **Student:** Chỉ truy cập chức năng dành cho sinh viên và dữ liệu Request, Attachment thuộc tài khoản của mình.
- **Staff:** Chỉ truy cập Request thuộc phạm vi được phân công hoặc phạm vi quyền được cấp.
- **Management:** Truy cập Dashboard, báo cáo và chức năng quản lý theo quyền được cấp.

Hệ thống phải kiểm tra quyền khi người dùng truy cập chức năng hoặc thực hiện thao tác với dữ liệu, bao gồm cả trường hợp truy cập trực tiếp bằng đường dẫn.

**Related Requirements:**
- FR-SEC-01
- NFR-SEC-01
- NFR-SEC-02
- NFR-SEC-03
- NFR-SEC-04

### 2. Access Restriction

Hệ thống phải từ chối các thao tác truy cập chức năng hoặc dữ liệu nằm ngoài phạm vi quyền của người sử dụng.

Các trường hợp cần kiểm soát:

- Student không được xem Request hoặc Attachment của Student khác.
- Staff không được xem hoặc cập nhật Request ngoài phạm vi được phân công hoặc quyền được cấp.
- Management không được truy cập chức năng hoặc dữ liệu ngoài quyền Management đã được cấu hình.
- Người dùng không có Role hoặc quyền phù hợp không được thực hiện thao tác bị hạn chế.
- Việc truy cập bằng URL trực tiếp không được bỏ qua cơ chế kiểm tra quyền.

**Related Requirements:**
- FR-SEC-01
- NFR-SEC-01
- NFR-SEC-02
- NFR-SEC-03
- NFR-SEC-04

### 3. Activity Logging and Audit Trail

Hệ thống ghi nhận các hoạt động quan trọng liên quan đến Request, thay đổi dữ liệu và truy cập thông tin để hỗ trợ theo dõi và kiểm tra.

Thông tin được ghi nhận bao gồm:

- Người thực hiện thao tác (Actor).
- Loại thao tác được thực hiện (Action).
- Thời điểm thực hiện (Timestamp).
- Đối tượng hoặc thông tin được thay đổi.
- Giá trị thay đổi liên quan khi cần thiết.

Các hoạt động quan trọng bao gồm thay đổi Request Status, Priority, Assignment và thông tin xử lý.

Lịch sử ghi nhận phải phản ánh đúng các thao tác đã được thực hiện và không ghi nhận thay đổi chưa được lưu thành công.

**Related Requirements:**
- FR-SEC-02
- NFR-SEC-05
- NFR-REL-02

### 4. User and Role Management

Hệ thống hỗ trợ các chức năng quản lý thông tin người dùng và Role theo quyền được cấp.

Phạm vi chức năng được mô tả trong Functional Requirements:

- Management xem thông tin người dùng và Role hiện tại.
- Management cập nhật Role của người dùng theo quyền được cấp.

**Scope Note:**

Việc triển khai và nghiệm thu các chức năng xem thông tin người dùng, cập nhật Role cần được xác nhận với Project Scope, Master Plan và WBS trước khi đưa vào phạm vi bàn giao chính thức.

**Related Requirements:**
- FR-SEC-01/AC-05
- FR-SEC-01/AC-06

### 5. Data Protection and Privacy

Hệ thống cần xem xét việc bảo vệ dữ liệu sinh viên trong quá trình truy cập, sử dụng và lưu trữ.

Các nội dung cần được kiểm soát:

- **User Authentication:** Người dùng phải được xác thực trước khi truy cập các chức năng yêu cầu quyền sử dụng.
- **Student Data Protection:** Chỉ người dùng có quyền phù hợp mới được truy cập thông tin sinh viên.
- **Attachment Protection:** Tài liệu đính kèm trong Request chỉ được truy cập bởi người có quyền tương ứng.
- **Data Retention:** Thời gian lưu trữ và cách xử lý dữ liệu phải tuân theo chính sách được Aurora University phê duyệt.
- **Sensitive Data Handling:** Dữ liệu nhạy cảm phải được xử lý theo quy định được xác nhận.

Prototype và testing chỉ sử dụng dữ liệu giả lập, không sử dụng dữ liệu cá nhân thật của sinh viên.

**Related Requirements:**
- NFR-SEC-02
- NFR-SEC-06
- NFR-SEC-07

## Related Requirements

### Functional Requirements

- [FR-SEC-01 – Role-Based Access Control and User Management](../../05-requirements/functional-requirements.md)
- [FR-SEC-02 – Audit Logging and Data Access Protection](../../05-requirements/functional-requirements.md)

### Non-Functional Requirements

- NFR-SEC-01 – Role-based Access
- NFR-SEC-02 – Student Data Access Protection
- NFR-SEC-03 – Staff Data Access Restriction
- NFR-SEC-04 – Management Access Restriction
- NFR-SEC-05 – Audit Logging
- NFR-SEC-06 – Data Retention and Sensitive Data Handling
- NFR-SEC-07 – Simulated Data Usage

### Related Documents

- [Users and Roles](../../02-domain/users-and-roles.md)
- [Functional Requirements](../../05-requirements/functional-requirements.md)
- [Non-Functional Requirements](../../05-requirements/non-functional-requirements.md)
- [Acceptance Criteria](../../06-acceptance/acceptance-criteria.md)
