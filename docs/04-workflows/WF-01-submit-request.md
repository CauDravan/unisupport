# WF-01 — Submit Request

## 1. Purpose

Mô tả quy trình Student gửi một yêu cầu hỗ trợ vào UniSupport và nhận xác nhận rằng yêu cầu đã được hệ thống tiếp nhận.

## 2. Actors

* **Primary Actor:** Student
* **System:** UniSupport

## 3. Trigger

Student cần gửi một yêu cầu hỗ trợ đến nhà trường.

## 4. Preconditions

* Student có thể truy cập UniSupport.
* Student đang ở Student Portal.
* Student có các thông tin cần thiết để mô tả yêu cầu.

## 5. Input

Student cung cấp:

* Request Type
* Subject
* Description
* Attachment (nếu có)
* Priority-related information nếu hệ thống yêu cầu xác định mức độ ưu tiên

Các loại yêu cầu có thể bao gồm:

* Course Registration
* Tuition
* Examination
* Student Verification

## 6. Main Flow

### Step 1 — Open Request Form

Student mở chức năng **Submit Request** trên Student Portal.

### Step 2 — Select Request Type

Student chọn loại yêu cầu phù hợp với vấn đề cần hỗ trợ.

### Step 3 — Enter Request Information

Student nhập các thông tin bắt buộc:

* Subject
* Request Type
* Description

Student có thể cung cấp thêm thông tin cần thiết để Staff hiểu và xử lý yêu cầu.

### Step 4 — Attach Supporting Documents

Student có thể đính kèm các tài liệu liên quan, chẳng hạn như hình ảnh hoặc PDF.

### Step 5 — Submit Request

Student kiểm tra thông tin và gửi yêu cầu.

Hệ thống kiểm tra các trường thông tin bắt buộc trước khi tạo request.

### Step 6 — Validate Request

Nếu thông tin bắt buộc còn thiếu, hệ thống không tạo request và thông báo cho Student biết thông tin cần bổ sung.

Nếu thông tin hợp lệ, hệ thống tiếp tục tạo request.

### Step 7 — Create Request

Hệ thống tạo một request mới và lưu các thông tin liên quan.

Request được ghi nhận với:

* Request ID
* Student ID
* Request Type
* Subject
* Description
* Attachment
* Created Date
* Status

### Step 8 — Confirm Submission

Hệ thống tạo **Request ID / Tracking ID** và hiển thị thông báo xác nhận rằng yêu cầu đã được tiếp nhận thành công.

Request bắt đầu ở trạng thái:

**Đã tiếp nhận (Received)**

## 7. Alternative Flows

### A1 — Missing Required Information

Nếu Student chưa nhập đầy đủ thông tin bắt buộc:

1. Hệ thống xác định các trường còn thiếu.
2. Hệ thống hiển thị thông báo cho Student.
3. Student bổ sung thông tin.
4. Student gửi lại request.

### A2 — Attachment Validation Failed

Nếu tệp đính kèm không đáp ứng yêu cầu của hệ thống:

1. Hệ thống từ chối tệp không hợp lệ.
2. Hệ thống thông báo lý do.
3. Student có thể xóa tệp hoặc chọn tệp khác.
4. Student tiếp tục gửi request.

## 8. Postconditions

### Successful

* Request được tạo thành công.
* Request có một Request ID duy nhất.
* Request được lưu với thông tin do Student cung cấp.
* Request có trạng thái **Đã tiếp nhận**.
* Student biết request đã được hệ thống tiếp nhận.

### Failed

* Request không được tạo.
* Thông tin Student nhập vẫn có thể được giữ lại trên form để Student chỉnh sửa và gửi lại.

## 9. Business Rules

* Request phải có các thông tin bắt buộc trước khi được tạo.
* Mỗi request phải có một Request ID.
* Request mới bắt đầu ở trạng thái **Đã tiếp nhận**.
* Attachment phải được liên kết với request tương ứng.
* Student chỉ có thể tạo request cho tài khoản của mình.
* Request và dữ liệu liên quan phải được bảo vệ theo quyền truy cập của người dùng.

## 10. Expected Outcome

Student gửi thành công một request và nhận được **Request ID** để sử dụng cho việc theo dõi request trong các workflow tiếp theo.

## 11. Related Requirements

* **FR-S1 — Request Submission**
* **FR-S2 — Request Tracking**
* **AC-01 — Student gửi yêu cầu đầy đủ**
* **AC-02 — Student gửi thông tin chưa đầy đủ**
* **AC-10 — Student kiểm tra yêu cầu**

## 12. Next Workflow

Sau khi request được tạo và tiếp nhận, request sẽ được chuyển sang:

**WF-02 — Classify and Assign**
