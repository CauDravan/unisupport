# Test Scenarios

## 1. Purpose

Tài liệu này mô tả các kịch bản kiểm thử dùng để xác minh Acceptance Criteria (AC) trong `functional-requirements.md` và Non-Functional Requirements (NFR) trong `non-functional-requirements.md` của hệ thống UniSupport.

Các kịch bản được xây dựng nhằm kiểm tra các chức năng trong phạm vi prototype, sử dụng dữ liệu giả lập và tuân theo các quy trình nghiệp vụ đã được xác định.

## 2. Test Conditions

- Sử dụng tài khoản và dữ liệu giả lập, không sử dụng dữ liệu cá nhân thật của sinh viên.
- Chuẩn bị các tài khoản thuộc ba vai trò Student, Staff và Management.
- Các trạng thái Request phải tuân theo `request-status.md`.
- Các thao tác nghiệp vụ phải đối chiếu với Workflow tương ứng.
- Những ngưỡng đo được đánh dấu Proposed baseline trong NFR cần được xác nhận trước khi sử dụng làm điều kiện nghiệm thu chính thức.

## 3. Functional Test Scenarios

### Student Portal – Request Submission

| Mã | Kiểm AC / NFR | Tiền điều kiện | Các bước | Kết quả mong đợi | Regression |
|---|---|---|---|---|---|
| TS-001 | FR-STU-01/AC-01 | Student đã đăng nhập. | Mở chức năng Submit Request và kiểm tra biểu mẫu. | Hệ thống hiển thị biểu mẫu cho phép nhập thông tin và lựa chọn Request Type. | Có |
| TS-002 | FR-STU-01/AC-02 | Student đã mở biểu mẫu gửi Request. | Để trống một trường bắt buộc và nhấn Submit. | Hệ thống không tạo Request và thông báo thông tin cần bổ sung. | Có |
| TS-003 | FR-STU-01/AC-03 | Student đã đăng nhập. | Gửi thành công hai Request hợp lệ và kiểm tra Request ID. | Mỗi Request được tạo có một Request ID duy nhất. | Có |
| TS-004 | FR-STU-01/AC-04 | Student đã mở biểu mẫu; Attachment không bắt buộc. | Điền thông tin hợp lệ nhưng không đính kèm tài liệu, sau đó Submit. | Hệ thống tiếp nhận Request thành công. | Có |
| TS-005 | FR-STU-01/AC-05 | Student đã mở biểu mẫu gửi Request. | Chọn tệp đính kèm không đáp ứng yêu cầu đã cấu hình và thực hiện Submit. | Hệ thống thông báo tệp không hợp lệ và không tiếp nhận tệp đó. | Có |
| TS-006 | FR-STU-01/AC-06 | Student đã đăng nhập. | Gửi một Request hợp lệ và kiểm tra thông báo sau khi gửi. | Student nhận được thông báo xác nhận Request đã được tiếp nhận. | Có |

## 4. Test Execution Record

Khi thực hiện kiểm thử, nhóm cần ghi nhận:

- Test Scenario ID.
- Ngày kiểm thử.
- Người thực hiện.
- Phiên bản prototype.
- Dữ liệu kiểm thử.
- Actual Result.
- Test Status: Pass / Fail / Blocked / Not Run.
- Evidence và Bug ID nếu có.