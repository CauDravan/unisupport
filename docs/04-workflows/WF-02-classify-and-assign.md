# WF-02 — Classify and Assign Request

## 1. Purpose

Quy trình này mô tả cách **Staff** phân loại request đã được tiếp nhận, xác định **Department** phù hợp và **assign request** cho Staff chịu trách nhiệm xử lý.

## 2. Actors

**Primary Actor:** Staff
**System:** UniSupport

## 3. Trigger

Quy trình bắt đầu khi một request mới đã được hệ thống tiếp nhận và sẵn sàng để Staff xử lý.

## 4. Preconditions

* Request đã được tạo thành công.
* Request có **Request ID**.
* Staff có quyền truy cập và xử lý request.
* Request chưa được assign cho Staff xử lý.

## 5. Input

* Request ID
* Request Type
* Subject
* Description
* Attachment (nếu có)
* Thông tin Student
* Thông tin Department và Staff có liên quan

## 6. Main Flow

### Step 1 — Review Request

Staff mở request và kiểm tra các thông tin do Student cung cấp.

### Step 2 — Classify Request

Staff xác định loại request dựa trên nội dung và thông tin của request.

### Step 3 — Identify Department

Staff xác định Department phù hợp để xử lý request.

### Step 4 — Assign Request

Staff assign request cho Staff phù hợp thuộc Department đã xác định.

### Step 5 — Record Assignment

System lưu thông tin assignment, bao gồm Department và Staff được assign.

### Step 6 — Update Request Status

System cập nhật request sang trạng thái phù hợp để tiếp tục quá trình xử lý.

### Step 7 — Record Request History

System ghi nhận thông tin classification và assignment vào lịch sử của request.

## 7. Alternative Flows

### A1 — Request Information Is Insufficient

Nếu thông tin trong request chưa đủ để xác định cách xử lý:

1. Staff kiểm tra phần thông tin còn thiếu.
2. Staff có thể chuyển sang workflow **WF-04 — Request Additional Information**.
3. Request được chuyển sang trạng thái **Waiting for Additional Information**.

### A2 — Request Assigned to Wrong Department

Nếu Staff xác định request không thuộc Department hiện tại:

1. Staff xác định Department phù hợp.
2. Request được chuyển sang Department phù hợp.
3. Assignment mới được ghi nhận trong lịch sử request.

### A3 — No Suitable Staff Available

Nếu chưa có Staff phù hợp để xử lý:

1. Request vẫn được giữ trong Department phù hợp.
2. Việc assignment được thực hiện khi Staff phù hợp được xác định.
3. Request tiếp tục được theo dõi cho đến khi được assign.

## 8. Postconditions

* Request đã được phân loại.
* Request đã được xác định Department xử lý.
* Request được assign cho Staff phù hợp, nếu Staff đã được xác định.
* Thông tin classification và assignment được lưu vào request history.
* Request sẵn sàng chuyển sang bước **Request Processing**.

## 9. Business Rules

* Mỗi request phải được xác định Department phù hợp trước khi được xử lý.
* Assignment phải được ghi nhận để xác định Staff chịu trách nhiệm xử lý request.
* Các thay đổi liên quan đến assignment phải được lưu trong request history.
* Việc chuyển request sang Department khác phải giữ lại lịch sử xử lý trước đó.
* Staff chỉ được thực hiện classification và assignment đối với request mà họ có quyền xử lý.

## 10. Expected Outcome

Sau khi hoàn thành workflow, request được **phân loại và assign đúng nơi xử lý**, đồng thời hệ thống lưu lại thông tin assignment để Staff tiếp tục xử lý và Management có thể theo dõi.

## 11. Related Requirements

* **Request Classification & Assignment**
* **FR-Support Workflow**
* **AC-03** — Staff receives new request.
* **AC-04** — Assignment is recorded.
* **AC-08** — Transferred request preserves previous history.

## 12. Next Workflow

**WF-03 — Process Request**
