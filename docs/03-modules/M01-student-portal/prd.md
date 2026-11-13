# M01 – Student Portal

## 1. Purpose

Student Portal là module dành cho Student, cho phép sinh viên gửi yêu cầu hỗ trợ, theo dõi tiến độ xử lý và tương tác với Staff trong quá trình giải quyết yêu cầu.

Module giúp Student biết yêu cầu đã được tiếp nhận hay chưa, theo dõi trạng thái xử lý, cung cấp thêm thông tin khi cần và gửi Feedback sau khi yêu cầu được giải quyết.

## 2. Users

### Primary User

- **Student:** Người gửi yêu cầu hỗ trợ, theo dõi tiến độ và tương tác với hệ thống.

### Supporting User

- **Staff:** Người xử lý yêu cầu và có thể gửi yêu cầu bổ sung thông tin cho Student. Staff thực hiện các thao tác xử lý thông qua M02 – Staff Workspace.

## 3. Main Capabilities

### 3.1 Submit Support Request

Student có thể gửi yêu cầu hỗ trợ thông qua hệ thống.

- Lựa chọn Request Type phù hợp.
- Nhập Subject và Description để mô tả vấn đề.
- Đính kèm tài liệu liên quan nếu cần.
- Gửi Request để hệ thống kiểm tra và tiếp nhận.
- Nhận thông báo xác nhận cùng Request ID sau khi gửi thành công.

**Expected Result:** Request được tạo và lưu vào hệ thống với một Request ID duy nhất. Student biết yêu cầu đã được tiếp nhận.

### 3.2 Track Request

Student có thể theo dõi các Request đã gửi thông qua tài khoản của mình.

- Xem danh sách Request đã gửi.
- Xem Request ID và Status hiện tại.
- Xem thông tin và lịch sử cập nhật của từng Request.
- Theo dõi kết quả xử lý, bao gồm trạng thái Resolved hoặc Closed.

**Expected Result:** Student có thể nắm được tình trạng hiện tại và lịch sử xử lý của từng Request thuộc tài khoản của mình.

### 3.3 Provide Additional Information

Student có thể cung cấp thêm thông tin khi Staff yêu cầu để tiếp tục xử lý Request.

- Nhận thông báo khi Request chuyển sang trạng thái Waiting for Additional Information.
- Xem nội dung và lý do Staff yêu cầu bổ sung.
- Cung cấp thông tin hoặc tài liệu bổ sung nếu cần.
- Gửi thông tin bổ sung để Staff tiếp tục xử lý.

**Expected Result:** Thông tin bổ sung được lưu vào đúng Request. Khi thông tin đã đầy đủ, Request có thể chuyển lại sang trạng thái In Progress theo workflow.

### 3.4 Receive Notifications

Student nhận thông báo liên quan đến các thay đổi trong quá trình xử lý Request.

- Nhận thông báo khi Status của Request thay đổi.
- Nhận thông báo khi Staff yêu cầu bổ sung thông tin.
- Nhận thông tin về kết quả xử lý và trạng thái hoàn tất của Request.

**Expected Result:** Student được cập nhật về những thay đổi quan trọng của Request mà không cần liên hệ Staff để hỏi tiến độ.

### 3.5 Submit Feedback

Student có thể gửi Feedback về kết quả hỗ trợ sau khi Request đã được xử lý và đóng.

- Mở Request có trạng thái Closed.
- Cung cấp Rating để đánh giá kết quả hỗ trợ.
- Nhập Comment nếu muốn chia sẻ thêm nhận xét.
- Gửi Feedback để hệ thống lưu lại.

**Expected Result:** Feedback được lưu và liên kết với Request tương ứng. Thông tin này có thể được sử dụng cho việc theo dõi chất lượng hỗ trợ và Management & Reporting.

## 4. Related Workflows

- [WF-01 – Submit Request](../../04-workflows/WF-01-submit-request.md)
- [WF-04 – Request Additional Information](../../04-workflows/WF-04-request-additional-information.md)
- [WF-06 – Resolve and Close Request](../../04-workflows/WF-06-resolve-and-close.md)
- [WF-07 – Feedback](../../04-workflows/WF-07-feedback.md)

## 5. Related Requirements

- [FR-STU-01 – Request Submission](../../05-requirements/functional-requirements.md#fr-stu-01--request-submission)
- [FR-STU-02 – Request Tracking and Notifications](../../05-requirements/functional-requirements.md#fr-stu-02--request-tracking-and-notifications)
- [FR-STU-03 – Additional Information and Feedback](../../05-requirements/functional-requirements.md#fr-stu-03--additional-information-and-feedback)

## 6. Related Modules

- **M02 – Staff Workspace:** Staff sử dụng module này để phân loại, tiếp nhận và xử lý Request do Student gửi.
- **M04 – Security and Access:** Kiểm soát đăng nhập, quyền truy cập và bảo vệ dữ liệu Request của Student.

## 7. Scope Notes

- Student chỉ được xem và thao tác trên các Request thuộc tài khoản của mình.
- Student có thể gửi Request có hoặc không có tệp đính kèm, tùy theo yêu cầu của từng Request.
- Feedback chỉ được gửi sau khi Request đã được xử lý và chuyển sang trạng thái Closed.
- Việc phân loại, assign, xử lý và đóng Request thuộc trách nhiệm của Staff thông qua M02, không thuộc phạm vi thao tác chính của Student Portal.