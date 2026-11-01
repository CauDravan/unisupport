# WF-03 — Process Request

## 1. Purpose

Mô tả quy trình **Staff** xử lý một request đã được assign, cập nhật tiến độ xử lý và đưa request đến trạng thái phù hợp.

## 2. Actors

* **Primary Actor:** Staff
* **System:** UniSupport

## 3. Trigger

Staff nhận được một request đã được assign và bắt đầu xử lý.

## 4. Preconditions

* Request đã được tạo và tiếp nhận.
* Request đã được classify.
* Request đã được assign cho Staff xử lý.
* Staff có quyền truy cập và xử lý request.

## 5. Input

Staff sử dụng các thông tin có sẵn trong request:

* Request ID
* Student ID
* Request Type
* Subject
* Description
* Attachment (nếu có)
* Department
* Assigned Staff
* Current Status

Staff có thể bổ sung thông tin xử lý trong quá trình giải quyết request.

## 6. Main Flow

### Step 1 — Open Assigned Request

Staff mở request đã được assign và kiểm tra thông tin do Student cung cấp.

### Step 2 — Review Request Information

Staff xem nội dung request, tài liệu đính kèm và các thông tin liên quan để xác định cách xử lý.

### Step 3 — Start Processing

Staff bắt đầu thực hiện các công việc cần thiết để giải quyết request.

System cập nhật request sang trạng thái:

**Đang xử lý (In Progress)**

### Step 4 — Update Processing Information

Trong quá trình xử lý, Staff cập nhật các thông tin cần thiết về tiến độ hoặc kết quả xử lý.

System lưu các cập nhật này vào request history.

### Step 5 — Check Additional Information

Staff kiểm tra xem request có cần Student cung cấp thêm thông tin hay không.

* Nếu không cần thêm thông tin, Staff tiếp tục xử lý.
* Nếu cần thêm thông tin, request được chuyển sang **WF-04 — Request Additional Information**.

### Step 6 — Complete Request Processing

Staff hoàn thành các công việc cần thiết để giải quyết request.

Staff ghi nhận kết quả xử lý vào request.

### Step 7 — Update Request Status

System cập nhật request sang trạng thái:

**Đã hoàn thành (Resolved)**

Thông tin thay đổi trạng thái được lưu vào request history.

## 7. Alternative Flows

### A1 — Additional Information Required

Nếu Staff cần thêm thông tin từ Student:

1. Staff xác định thông tin cần bổ sung.
2. Request được chuyển sang **WF-04 — Request Additional Information**.
3. Request chuyển sang trạng thái **Waiting for Additional Information**.
4. Sau khi Student cung cấp thông tin, Staff tiếp tục xử lý request.

### A2 — Request Cannot Be Resolved by Current Staff

Nếu Staff không thể tiếp tục xử lý request:

1. Staff xác định lý do request cần được chuyển.
2. Request được chuyển sang **WF-05 — Transfer Request**.
3. Department hoặc Staff mới tiếp tục xử lý request.
4. Lịch sử xử lý trước đó được giữ lại.

### A3 — Processing Is Not Completed

Nếu Staff chưa thể hoàn thành request:

1. Staff tiếp tục cập nhật thông tin xử lý khi cần.
2. Request vẫn ở trạng thái **In Progress**.
3. Staff tiếp tục xử lý cho đến khi request được giải quyết hoặc cần chuyển sang workflow khác.

## 8. Postconditions

### Successful

* Request đã được Staff xử lý.
* Kết quả xử lý được ghi nhận.
* Request chuyển sang trạng thái **Đã hoàn thành (Resolved)**.
* Các cập nhật trong quá trình xử lý được lưu vào request history.

### Not Completed

* Request vẫn ở trạng thái **Đang xử lý (In Progress)**, hoặc
* Request được chuyển sang workflow phù hợp nếu cần thêm thông tin hoặc cần transfer.

## 9. Business Rules

* Chỉ Staff được assign cho request hoặc Staff có quyền phù hợp mới được xử lý request.
* Staff phải cập nhật trạng thái khi request thay đổi trong quá trình xử lý.
* Các thông tin cập nhật và thay đổi trạng thái phải được lưu vào request history.
* Khi cần thêm thông tin từ Student, request phải chuyển sang trạng thái **Waiting for Additional Information**.
* Sau khi Student cung cấp thông tin cần thiết, Staff có thể tiếp tục xử lý request.
* Request chỉ được chuyển sang **Resolved** khi Staff đã hoàn thành việc xử lý.

## 10. Expected Outcome

Request được Staff xử lý và cập nhật đầy đủ tiến độ. Khi công việc hoàn tất, request được chuyển sang **Resolved** và kết quả xử lý được lưu lại để Student có thể theo dõi.

## 11. Related Requirements

* [FR-St2 — Request Processing & Escalation](../05-requirements/functional-requirements.md#fr-st2-processing-and-escalation)
* [AC-05 — Staff thay đổi Request Status](../07-acceptance/acceptance-criteria.md#ac-05)

* [AC-06 — Staff yêu cầu Student bổ sung thông tin](../07-acceptance/acceptance-criteria.md#ac-06)
* [AC-07 — Student cung cấp thông tin bổ sung](../07-acceptance/acceptance-criteria.md#ac-07)
* [AC-08 — Staff chuyển giao Request](../07-acceptance/acceptance-criteria.md#ac-08)

## 12. Next Workflow

Sau khi request được xử lý và chuyển sang **Resolved**, request sẽ được chuyển sang:

* [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)
