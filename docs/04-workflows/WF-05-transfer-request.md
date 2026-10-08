# WF-05 — Transfer Request

## 1. Purpose

Mô tả quy trình **Staff** chuyển một request sang **Department hoặc Staff khác** khi request không phù hợp hoặc không thể tiếp tục được xử lý bởi người đang phụ trách.

## 2. Actors

* **Primary Actor:** Staff
* **System:** UniSupport

## 3. Trigger

Staff đang xử lý request và xác định request cần được chuyển sang Department hoặc Staff khác.

## 4. Preconditions

* Request đã được tạo và tiếp nhận.
* Request đã được assign cho Staff.
* Staff hiện tại có quyền chuyển request.
* Department hoặc Staff phù hợp để tiếp nhận request có thể được xác định.

## 5. Input

Staff cung cấp hoặc xác định:

* Request ID
* Department mới
* Staff mới (nếu đã xác định)
* Lý do transfer
* Thông tin liên quan đến việc chuyển request

## 6. Main Flow

### Step 1 — Review Request

Staff kiểm tra request và xác định rằng request cần được chuyển sang nơi xử lý khác.

### Step 2 — Identify Transfer Destination

Staff xác định **Department** hoặc **Staff** phù hợp để tiếp nhận request.

### Step 3 — Provide Transfer Reason

Staff ghi nhận lý do cần transfer request.

Lý do giúp Staff tiếp nhận hiểu được tại sao request được chuyển.

### Step 4 — Transfer Request

Staff thực hiện transfer request đến Department hoặc Staff đã xác định.

### Step 5 — Update Assignment

System cập nhật thông tin assignment của request.

Thông tin Department và Staff mới được ghi nhận trên request.

### Step 6 — Preserve Request History

System giữ lại toàn bộ lịch sử xử lý trước đó của request.

Lịch sử transfer mới được thêm vào request history.

### Step 7 — Notify Relevant Staff

System cập nhật request để Staff mới có thể tiếp nhận và tiếp tục xử lý.

### Step 8 — Continue Processing

Staff mới tiếp nhận request và tiếp tục xử lý theo:

**WF-03 — Process Request**

## 7. Alternative Flows

### A1 — No Suitable Destination

Nếu chưa xác định được Department hoặc Staff phù hợp:

1. Staff chưa thực hiện transfer.
2. Request tiếp tục được giữ tại nơi đang xử lý.
3. Staff tiếp tục xác định nơi xử lý phù hợp.

### A2 — Transfer to Another Department

Nếu request cần được chuyển sang Department khác:

1. Staff xác định Department mới.
2. System cập nhật Department của request.
3. Assignment mới được ghi nhận.
4. Request tiếp tục được xử lý bởi Department mới.

### A3 — Transfer to Another Staff

Nếu request vẫn thuộc cùng Department nhưng cần Staff khác xử lý:

1. Staff xác định Staff mới.
2. System cập nhật Assigned Staff.
3. Assignment mới được ghi nhận.
4. Staff mới tiếp tục xử lý request.

## 8. Postconditions

### Successful

* Request đã được chuyển đến Department hoặc Staff mới.
* Assignment mới được ghi nhận.
* Lý do transfer được lưu lại.
* Lịch sử xử lý trước đó vẫn được giữ nguyên.
* Request sẵn sàng được Staff mới tiếp tục xử lý.

### Not Completed

* Request vẫn thuộc Staff hoặc Department hiện tại.
* Không có assignment mới được tạo.

## 9. Business Rules

* Request chỉ được transfer bởi Staff có quyền phù hợp.
* Transfer phải xác định được Department hoặc Staff tiếp nhận.
* Lý do transfer phải được ghi nhận.
* Assignment mới phải được lưu vào request.
* Lịch sử xử lý trước khi transfer không được mất.
* Mọi thay đổi liên quan đến transfer phải được lưu vào request history.

## 10. Expected Outcome

Request được chuyển đến **Department hoặc Staff phù hợp**, đồng thời toàn bộ lịch sử xử lý trước đó được giữ lại. Staff mới có thể tiếp tục xử lý request mà không làm mất thông tin của quá trình xử lý trước.

## 11. Related Requirements

* **Request Classification & Assignment**
* **Request Processing**
* **AC-04 — Assignment is recorded**
* **AC-08 — Transferred request preserves previous history**

## 12. Next Workflow

Sau khi transfer thành công, request sẽ được tiếp tục xử lý theo:

**WF-03 — Process Request**
