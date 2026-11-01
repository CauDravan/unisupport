# WF-06 — Resolve and Close Request

## 1. Purpose

Mô tả quy trình **Staff** hoàn thành việc xử lý request, ghi nhận kết quả và đóng request sau khi request đã được giải quyết.

## 2. Actors

* **Primary Actor:** Staff
* **System:** UniSupport

## 3. Trigger

Staff hoàn thành việc xử lý request và xác định rằng yêu cầu của Student đã được giải quyết.

## 4. Preconditions

* Request đã được Staff xử lý.
* Request đang ở trạng thái **Đang xử lý (In Progress)**.
* Staff có đủ thông tin để ghi nhận kết quả xử lý.
* Không còn thông tin bắt buộc nào đang chờ Student bổ sung.

## 5. Input

Staff cung cấp:

* Request ID
* Resolution / Kết quả xử lý
* Thông tin cần thiết để hoàn tất request

System sử dụng thông tin request hiện tại để cập nhật trạng thái và lưu lịch sử.

## 6. Main Flow

### Step 1 — Complete Request Processing

Staff hoàn thành các công việc cần thiết để giải quyết request.

### Step 2 — Record Resolution

Staff ghi nhận kết quả xử lý của request.

Thông tin này cho biết request đã được giải quyết như thế nào.

### Step 3 — Mark Request as Resolved

System cập nhật request sang trạng thái:

**Đã hoàn thành (Resolved)**

Thay đổi trạng thái và kết quả xử lý được lưu vào request history.

### Step 4 — Review Resolution

Staff kiểm tra lại kết quả xử lý và xác nhận request đã có thể được hoàn tất.

### Step 5 — Close Request

Staff thực hiện đóng request.

System cập nhật request sang trạng thái:

**Đã đóng (Closed)**

### Step 6 — Record Closure

System lưu thông tin đóng request, bao gồm:

* Closed Date
* Current Status
* Resolution
* Request History

### Step 7 — Notify Student

System cập nhật thông tin request để Student có thể biết request đã được hoàn tất và đóng.

## 7. Alternative Flows

### A1 — Request Is Not Resolved

Nếu Staff xác định request chưa được giải quyết hoàn toàn:

1. Staff không chuyển request sang **Resolved**.
2. Request tiếp tục ở trạng thái **In Progress**.
3. Staff tiếp tục xử lý theo **WF-03 — Process Request**.

### A2 — Resolution Requires Additional Information

Nếu Staff nhận thấy vẫn cần thông tin từ Student:

1. Staff không đóng request.
2. Request được chuyển sang **WF-04 — Request Additional Information**.
3. Request chuyển sang trạng thái **Waiting for Additional Information**.
4. Sau khi có đủ thông tin, Staff tiếp tục xử lý request.

### A3 — Request Requires Transfer

Nếu Staff xác định request cần được xử lý bởi Department hoặc Staff khác:

1. Staff không đóng request.
2. Request được chuyển sang **WF-05 — Transfer Request**.
3. Staff mới tiếp tục xử lý request.

## 8. Postconditions

### Successful

* Request đã có kết quả xử lý.
* Request được chuyển sang **Resolved**.
* Resolution được lưu lại.
* Request được chuyển sang **Closed**.
* Closed Date được ghi nhận.
* Toàn bộ lịch sử xử lý được giữ lại.
* Student có thể xem trạng thái cuối cùng của request.

### Not Completed

* Request chưa được đóng.
* Request tiếp tục ở **In Progress** hoặc chuyển sang workflow phù hợp.

## 9. Business Rules

* Request chỉ được chuyển sang **Resolved** khi Staff đã hoàn thành việc xử lý.
* Resolution phải được ghi nhận trước khi request được đóng.
* Request phải ở trạng thái **Resolved** trước khi chuyển sang **Closed**.
* Closed Date phải được ghi nhận khi request được đóng.
* Các thay đổi về status và resolution phải được lưu vào request history.
* Request đã **Closed** không tiếp tục được xử lý như một request đang hoạt động.

## 10. Expected Outcome

Request được giải quyết và đóng thành công. System lưu lại **Resolution, Closed Date, Status và Request History**, cho phép Student theo dõi kết quả cuối cùng của request.

## 11. Related Requirements

* [FR-St2 — Request Processing & Escalation](../05-requirements/functional-requirements.md#fr-st2-processing-and-escalation)
* [FR-S2 — Request Tracking](../05-requirements/functional-requirements.md#fr-s2-request-tracking)

* [AC-05 — Staff thay đổi Request Status](../07-acceptance/acceptance-criteria.md#ac-05)
* [AC-09 — Staff hoàn tất và đóng Request](../07-acceptance/acceptance-criteria.md#ac-09)
* [AC-10 — Student kiểm tra Request](../07-acceptance/acceptance-criteria.md#ac-10)

## 12. Next Workflow

Sau khi request được đóng:

* [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)
