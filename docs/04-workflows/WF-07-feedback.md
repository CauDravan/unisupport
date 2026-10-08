# WF-07 — Feedback

## 1. Purpose

Mô tả quy trình **Student** gửi feedback về kết quả hỗ trợ sau khi request đã được giải quyết và đóng.

## 2. Actors

* **Primary Actor:** Student
* **System:** UniSupport

## 3. Trigger

Student muốn đánh giá hoặc gửi nhận xét về kết quả xử lý của một request đã được đóng.

## 4. Preconditions

* Request đã được xử lý.
* Request đang ở trạng thái **Đã đóng (Closed)**.
* Student là người đã gửi request.
* Student có quyền xem request và gửi feedback.

## 5. Input

Student cung cấp:

* Request ID
* Rating / Mức đánh giá
* Comment / Nhận xét (nếu có)

## 6. Main Flow

### Step 1 — Open Closed Request

Student mở request đã được đóng và xem kết quả xử lý.

### Step 2 — Open Feedback

Student chọn chức năng **Feedback** cho request.

### Step 3 — Provide Feedback

Student cung cấp:

* Rating về kết quả hỗ trợ.
* Comment nếu muốn cung cấp thêm nhận xét.

### Step 4 — Submit Feedback

Student kiểm tra thông tin và gửi feedback.

System kiểm tra thông tin feedback trước khi lưu.

### Step 5 — Validate Feedback

Nếu feedback hợp lệ, System tiếp tục lưu feedback.

Nếu thông tin không hợp lệ, System thông báo cho Student để chỉnh sửa.

### Step 6 — Save Feedback

System lưu feedback và liên kết feedback với request tương ứng.

### Step 7 — Confirm Feedback

System thông báo cho Student rằng feedback đã được gửi thành công.

### Step 8 — Record Feedback

System ghi nhận feedback để có thể sử dụng cho việc theo dõi và báo cáo.

## 7. Alternative Flows

### A1 — Invalid Feedback

Nếu feedback không đáp ứng yêu cầu của System:

1. System không lưu feedback.
2. System thông báo cho Student biết thông tin cần chỉnh sửa.
3. Student cập nhật feedback.
4. Student gửi lại feedback.

### A2 — Student Does Not Provide Comment

Nếu Student không muốn viết nhận xét:

1. Student chỉ cung cấp Rating.
2. System lưu feedback với Rating đã cung cấp.
3. Feedback được ghi nhận thành công.

### A3 — Student Does Not Submit Feedback

Nếu Student không gửi feedback:

1. Request vẫn giữ trạng thái **Closed**.
2. Không có feedback mới được lưu.
3. Request không bị ảnh hưởng bởi việc Student không gửi feedback.

## 8. Postconditions

### Successful

* Feedback được tạo thành công.
* Feedback được liên kết với request tương ứng.
* Rating và Comment được lưu nếu Student cung cấp.
* Feedback có thể được sử dụng cho Management & Reporting.

### Not Completed

* Không có feedback mới được lưu.
* Request vẫn giữ trạng thái **Closed**.

## 9. Business Rules

* Feedback phải được liên kết với request tương ứng.
* Chỉ Student có quyền phù hợp mới được gửi feedback cho request của mình.
* Feedback chỉ được gửi sau khi request đã được xử lý và đóng.
* Rating phải đáp ứng các giá trị mà System cho phép.
* Comment là thông tin bổ sung và có thể không bắt buộc.
* Feedback phải được lưu để phục vụ việc theo dõi và báo cáo.

## 10. Expected Outcome

Student gửi feedback về kết quả hỗ trợ. System lưu feedback cùng với request tương ứng, giúp **Management** có thêm thông tin để theo dõi chất lượng hỗ trợ và phục vụ báo cáo.

## 11. Related Requirements

* **Management & Reporting**
* **AC-14 — Feedback is stored**
* **AC-10 — Student checks request**

## 12. Next Workflow

**End of Request Workflow**
