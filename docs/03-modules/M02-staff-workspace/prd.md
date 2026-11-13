# M02 – Staff Workspace

## 1. Purpose

Staff Workspace là module dành cho Staff để quản lý và xử lý các Request được gửi đến Department mà Staff phụ trách hoặc được cấp quyền truy cập.

Module hỗ trợ Staff theo dõi Request Queue, phân loại và phân công Request, cập nhật tiến độ xử lý, yêu cầu Student bổ sung thông tin, chuyển Request khi cần thiết và ghi nhận kết quả xử lý trước khi đóng Request.

## 2. Users

### Primary User

- **Staff:** Người tiếp nhận, phân loại, phân công và xử lý Request trong phạm vi quyền hạn được cấp.

### Supporting User

- **Student:** Người cung cấp thêm thông tin hoặc tài liệu khi Staff yêu cầu thông qua Student Portal.

## 3. Main Capabilities

### 3.1 View Request Queue

Staff có thể xem và quản lý danh sách Request thông qua một hàng đợi tập trung trong phạm vi được cấp quyền.

Module hỗ trợ Staff:

- Xem các Request cần phân loại hoặc phân công.
- Xem các Request thuộc phạm vi cá nhân hoặc Department được phân công.
- Xem thông tin tổng quan của từng Request, bao gồm Request ID, Request Type, Status và Priority.
- Lọc Request theo Status hoặc Priority.
- Theo dõi thời gian chờ của từng Request.
- Mở Request để xem thông tin chi tiết và tiếp tục xử lý.

**Expected Result:** Staff có thể xác định các Request cần phân loại, phân công hoặc tiếp tục xử lý. Danh sách chỉ hiển thị Request thuộc phạm vi quyền truy cập của Staff.

### 3.2 Classify and Assign Request

Staff có thể phân loại Request và xác định Department cùng người chịu trách nhiệm xử lý.

Staff thực hiện:

- Kiểm tra nội dung và thông tin do Student cung cấp.
- Xác định Request Type phù hợp.
- Xác định Priority dựa trên mức độ ảnh hưởng và tính cấp thiết của Request.
- Lựa chọn Department chịu trách nhiệm xử lý.
- Assign Request cho Staff phù hợp.
- Xác nhận và lưu thông tin Classification và Assignment.

**Expected Result:** Request được phân loại và chuyển đến Department phù hợp, có Staff chịu trách nhiệm cụ thể. Thông tin Classification và Assignment được lưu vào Request History.

### 3.3 Process Request

Staff có thể xử lý Request đã được phân công và cập nhật tiến độ trong quá trình giải quyết.

Staff thực hiện:

- Xem nội dung, thông tin Student và tài liệu đính kèm của Request.
- Kiểm tra lịch sử xử lý trước đó.
- Bắt đầu xử lý và cập nhật Status theo tiến độ thực tế.
- Ghi nhận nội dung và hoạt động xử lý vào Activity Log.
- Kiểm tra xem có cần Student bổ sung thông tin hay cần chuyển Request hay không.
- Ghi nhận kết quả xử lý khi hoàn thành.

**Expected Result:** Request được cập nhật đúng tiến độ. Các hoạt động và thay đổi quan trọng được lưu lại để Staff và các User có quyền phù hợp có thể theo dõi.

### 3.4 Request Additional Information

Staff có thể yêu cầu Student bổ sung thông tin hoặc tài liệu khi thông tin hiện tại chưa đủ để tiếp tục xử lý Request.

Staff thực hiện:

- Xác định thông tin hoặc tài liệu còn thiếu.
- Ghi rõ nội dung cần Student bổ sung.
- Gửi yêu cầu bổ sung thông tin.
- Theo dõi thông tin Student gửi lại.

System thực hiện:

- Cập nhật Request sang trạng thái Waiting for Additional Information.
- Thông báo cho Student về yêu cầu bổ sung.
- Lưu yêu cầu và thông tin bổ sung vào Request History.
- Cập nhật Request về trạng thái In Progress sau khi Student cung cấp đủ thông tin theo quy trình.

**Expected Result:** Student biết thông tin cần bổ sung. Staff có thể tiếp tục xử lý Request sau khi nhận được thông tin cần thiết.

### 3.5 Transfer Request

Staff có thể chuyển Request sang Department hoặc Staff khác khi Request cần được xử lý bởi đơn vị hoặc người phù hợp hơn.

Staff thực hiện:

- Kiểm tra Request và xác định lý do cần chuyển.
- Xác định Department hoặc Staff tiếp nhận.
- Ghi nhận lý do Transfer.
- Thực hiện chuyển Request đến nơi tiếp nhận phù hợp.

System thực hiện:

- Cập nhật Department và Assigned Staff mới.
- Giữ lại thông tin và tài liệu đính kèm của Request.
- Bảo toàn lịch sử xử lý trước đó.
- Ghi nhận hoạt động Transfer vào Request History.

**Expected Result:** Request được chuyển đến đúng nơi tiếp nhận. Staff mới có thể tiếp tục xử lý mà không làm mất thông tin hoặc lịch sử trước đó.

### 3.6 Resolve and Close Request

Staff có thể hoàn tất việc xử lý Request, ghi nhận kết quả và đóng Request theo quy trình.

Staff thực hiện:

- Kiểm tra Request đã được giải quyết hay chưa.
- Ghi nhận Resolution mô tả kết quả xử lý.
- Xác nhận Request đã đáp ứng điều kiện để hoàn tất.
- Thực hiện đóng Request sau khi Request được chuyển sang trạng thái Resolved.

System thực hiện:

- Cập nhật Request sang trạng thái Resolved.
- Cập nhật Request sang trạng thái Closed khi Staff thực hiện đóng.
- Ghi nhận Resolution và Closed Date.
- Lưu các thay đổi vào Request History.
- Cập nhật thông tin để Student có thể theo dõi kết quả cuối cùng.

**Expected Result:** Request được giải quyết và đóng theo đúng trình tự. Resolution, Status, Closed Date và Request History được lưu lại để phục vụ việc theo dõi.

## 4. Related Workflows

- [WF-02 – Classify and Assign Request](../../04-workflows/WF-02-classify-and-assign.md)
- [WF-03 – Process Request](../../04-workflows/WF-03-process-request.md)
- [WF-04 – Request Additional Information](../../04-workflows/WF-04-request-additional-information.md)
- [WF-05 – Transfer Request](../../04-workflows/WF-05-transfer-request.md)
- [WF-06 – Resolve and Close Request](../../04-workflows/WF-06-resolve-and-close.md)

## 5. Related Functional Requirements

- [FR-STA-01 – Request Classification and Assignment](../../05-requirements/functional-requirements.md#fr-sta-01--request-classification-and-assignment)
- [FR-STA-02 – Queue Management](../../05-requirements/functional-requirements.md#fr-sta-02--queue-management)
- [FR-STA-03 – Request Processing, Transfer and Resolution](../../05-requirements/functional-requirements.md#fr-sta-03--request-processing-transfer-and-resolution)

## 6. Related Acceptance Criteria

- [AC-03 – Staff nhận Request mới](../../06-acceptance/acceptance-criteria.md#ac-03)
- [AC-04 – Staff phân công Request](../../06-acceptance/acceptance-criteria.md#ac-04)
- [AC-05 – Staff thay đổi Request Status](../../06-acceptance/acceptance-criteria.md#ac-05)
- [AC-06 – Staff yêu cầu Student bổ sung thông tin](../../06-acceptance/acceptance-criteria.md#ac-06)
- [AC-08 – Staff chuyển giao Request](../../06-acceptance/acceptance-criteria.md#ac-08)
- [AC-09 – Staff hoàn tất và đóng Request](../../06-acceptance/acceptance-criteria.md#ac-09)

## 7. Related Modules

- **M01 – Student Portal:** Student sử dụng module này để gửi Request, theo dõi Status, nhận thông báo và cung cấp thông tin bổ sung.
- **M03 – Management Dashboard:** Management sử dụng thông tin Request và hoạt động xử lý để theo dõi tình hình hoạt động và hiệu suất hỗ trợ.
- **M04 – Security and Access:** Kiểm soát quyền truy cập của Staff đối với Request và các chức năng trong Staff Workspace.