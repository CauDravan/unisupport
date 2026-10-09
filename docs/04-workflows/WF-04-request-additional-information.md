# WF-04 — Request Additional Information

## 1. Purpose

Mô tả quy trình **Staff** yêu cầu **Student** bổ sung thông tin cần thiết để tiếp tục xử lý request.

## 2. Actors

* **Primary Actor:** Staff
* **Supporting Actor:** Student
* **System:** UniSupport

## 3. Trigger

Staff đang xử lý request nhưng nhận thấy thông tin hiện tại chưa đủ để tiếp tục xử lý.

## 4. Preconditions

* Request đã được tạo và tiếp nhận.
* Request đã được assign cho Staff.
* Staff đang xử lý request.
* Staff xác định request cần thêm thông tin từ Student.

## 5. Input

Staff xác định:

* Request ID
* Thông tin cần Student bổ sung
* Lý do cần bổ sung thông tin
* Supporting documents nếu cần

Student cung cấp thông tin hoặc tài liệu được yêu cầu.

## 6. Main Flow

### Step 1 — Identify Missing Information

Staff kiểm tra request và xác định thông tin còn thiếu hoặc chưa đủ để tiếp tục xử lý.

### Step 2 — Request Additional Information

Staff gửi yêu cầu bổ sung thông tin cho Student.

System ghi nhận yêu cầu và cập nhật request sang trạng thái:

**Chờ bổ sung thông tin (Waiting for Additional Information)**

### Step 3 — Notify Student

System thông báo cho Student rằng request cần được bổ sung thông tin.

Student có thể xem nội dung yêu cầu và biết thông tin cần cung cấp.

### Step 4 — Provide Additional Information

Student mở request và cung cấp thông tin được yêu cầu.

Student có thể đính kèm tài liệu bổ sung nếu cần.

### Step 5 — Submit Additional Information

Student gửi thông tin bổ sung cho System.

System lưu thông tin bổ sung vào request.

### Step 6 — Resume Processing

System ghi nhận Student đã cung cấp thông tin.

Request quay lại trạng thái:

**Đang xử lý (In Progress)**

Staff tiếp tục xử lý request dựa trên thông tin mới được cung cấp.

### Step 7 — Record Request History

System lưu lại:

* Yêu cầu bổ sung thông tin.
* Thông tin Student đã cung cấp.
* Các thay đổi trạng thái liên quan.

## 7. Alternative Flows

### A1 — Student Has Not Provided Information

Nếu Student chưa cung cấp thông tin:

1. Request vẫn ở trạng thái **Waiting for Additional Information**.
2. Staff chưa thể tiếp tục xử lý phần việc phụ thuộc vào thông tin còn thiếu.
3. Request tiếp tục được theo dõi cho đến khi Student cung cấp thông tin.

### A2 — Student Provides Incomplete Information

Nếu thông tin Student cung cấp vẫn chưa đủ:

1. Staff kiểm tra thông tin mới.
2. Staff xác định phần thông tin còn thiếu.
3. Staff gửi yêu cầu bổ sung thêm thông tin.
4. Request tiếp tục ở trạng thái **Waiting for Additional Information**.

### A3 — Student Provides Sufficient Information

Nếu thông tin Student cung cấp đã đầy đủ:

1. System lưu thông tin bổ sung.
2. Request chuyển sang **In Progress**.
3. Staff tiếp tục xử lý request.

## 8. Postconditions

### Successful

* Student đã cung cấp thông tin được yêu cầu.
* Thông tin bổ sung được lưu vào request.
* Request chuyển lại sang **In Progress**.
* Staff có đủ thông tin để tiếp tục xử lý.
* Các hoạt động liên quan được lưu vào request history.

### Not Completed

* Request vẫn ở trạng thái **Waiting for Additional Information**.
* Staff chưa thể hoàn thành phần xử lý phụ thuộc vào thông tin còn thiếu.

## 9. Business Rules

* Staff phải xác định rõ thông tin cần Student bổ sung.
* Khi yêu cầu bổ sung thông tin được tạo, request phải chuyển sang **Waiting for Additional Information**.
* Student phải được thông báo khi request cần bổ sung thông tin.
* Thông tin Student cung cấp phải được lưu cùng request tương ứng.
* Sau khi Student cung cấp đủ thông tin, request có thể quay lại **In Progress**.
* Các yêu cầu bổ sung và thông tin được cung cấp phải được lưu vào request history.

## 10. Expected Outcome

Student cung cấp đủ thông tin cần thiết để Staff tiếp tục xử lý request. Request chuyển từ **Waiting for Additional Information** về **In Progress**, đồng thời toàn bộ quá trình bổ sung thông tin được lưu lại trong request history.

## 11. Related Requirements

* [FR-St2 — Request Processing & Escalation](../05-requirements/functional-requirements.md#fr-st2-processing-and-escalation)
* [FR-S3 — Additional Information & Feedback](../05-requirements/functional-requirements.md#fr-s3-additional-information-feedback)

* [AC-06 — Staff yêu cầu Student bổ sung thông tin](../07-acceptance/acceptance-criteria.md#ac-06)
* [AC-07 — Student cung cấp thông tin bổ sung](../07-acceptance/acceptance-criteria.md#ac-07)

## 12. Next Workflow

Sau khi Student cung cấp đủ thông tin, request quay lại:

* [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)
