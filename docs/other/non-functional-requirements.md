# Non-Functional Requirements

Các yêu cầu phi chức năng xác định các tiêu chí về hiệu năng, khả năng sử dụng,
bảo mật và độ tin cậy mà hệ thống UniSupport cần đáp ứng trong phạm vi prototype.

---

## 1. Performance

Hệ thống cần có hiệu năng phù hợp với các thao tác chính và dữ liệu mô phỏng
được sử dụng trong quá trình phát triển và trình diễn prototype.

### Requirements

- Hệ thống cần có thời gian phản hồi ở mức chấp nhận được đối với các thao tác
  thông thường như gửi Request, xem trạng thái và truy cập Dashboard.
- Hệ thống cần hạn chế các request không cần thiết đến server để tránh ảnh hưởng
  đến hiệu năng.
- Hệ thống cần có khả năng xử lý bộ dữ liệu mô phỏng được sử dụng trong quá
  trình phát triển và trình diễn prototype.
- Các yêu cầu về khả năng chịu tải ở quy mô lớn và kiểm thử hiệu năng production
  không thuộc phạm vi của prototype hiện tại.

---

## 2. Usability

Hệ thống cần có giao diện rõ ràng và dễ sử dụng đối với Student, Staff và
Management.

### Requirements

- Giao diện cần rõ ràng và dễ sử dụng đối với các nhóm người dùng chính.
- Các thao tác chính như gửi Request, theo dõi Status và xử lý Request cần có
  quy trình trực quan và dễ hiểu.
- Hệ thống cần hỗ trợ giao diện trên cả máy tính và thiết bị di động.
- Status, Notification và các thông tin quan trọng của Request cần được trình
  bày rõ ràng để người dùng dễ theo dõi.

---

## 3. Security & Access Control

Hệ thống cần kiểm soát quyền truy cập dựa trên Role và bảo vệ dữ liệu khỏi
truy cập trái phép.

### Requirements

- Người dùng chỉ được truy cập các chức năng và dữ liệu phù hợp với Role của mình.
- Student chỉ được xem và thao tác với các Request thuộc tài khoản của mình.
- Staff chỉ được truy cập các Request thuộc phạm vi được phân công.
- Management có quyền truy cập các chức năng và dữ liệu phục vụ việc giám sát
  và báo cáo theo phạm vi được cấp.
- Các dữ liệu liên quan đến Request và thông tin người dùng cần được bảo vệ khỏi
  truy cập trái phép.
- Các hoạt động cần thiết cho việc kiểm tra và giám sát hệ thống cần được ghi nhận.

---

## 4. Reliability & Data Integrity

Hệ thống cần duy trì tính nhất quán và toàn vẹn của dữ liệu trong quá trình
xử lý Request.

### Requirements

- Dữ liệu Request cần được duy trì nhất quán trong suốt vòng đời xử lý.
- Các thay đổi về Status, Priority và hoạt động xử lý cần được ghi nhận để
  phục vụ việc theo dõi.
- Khi Request được Transfer sang Staff hoặc Department khác, dữ liệu liên quan,
  bao gồm Attachment và lịch sử xử lý, cần được bảo toàn.
- Dữ liệu Feedback cần được lưu trữ để phục vụ việc đánh giá và báo cáo.
- Prototype sử dụng dữ liệu mô phỏng thay cho dữ liệu cá nhân thực tế.