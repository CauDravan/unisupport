# M02 – Staff Workspace

## Mục đích

Không gian làm việc dành cho nhân viên để **tiếp nhận, phân loại, phân công và xử lý các yêu cầu hỗ trợ** được gửi đến phòng ban.

## Người sử dụng

* Nhân viên

## Chức năng chính

### 1. View Request Queue

Nhân viên có thể xem các yêu cầu thuộc phòng ban của mình trên một giao diện tập trung. Danh sách hiển thị các thông tin cần thiết để nhân viên xác định yêu cầu cần xử lý.

Nhân viên có thể:

* Lọc yêu cầu theo mức độ ưu tiên.
* Lọc yêu cầu theo trạng thái.
* Xem thời gian chờ của từng yêu cầu.

### 2. Classify and Assign Request

Nhân viên có thể phân loại yêu cầu và xác định phòng ban hoặc nhân viên chịu trách nhiệm xử lý.

Nhân viên có thể:

* Xác định loại yêu cầu.
* Xác định mức độ ưu tiên.
* Phân công yêu cầu cho nhân viên phù hợp.
* Theo dõi người hoặc phòng ban đang chịu trách nhiệm.

### 3. Process Request

Nhân viên có thể xử lý các yêu cầu được phân công và cập nhật tiến độ xử lý.

Nhân viên có thể:

* Xem nội dung và tài liệu đính kèm của yêu cầu.
* Cập nhật trạng thái yêu cầu.
* Ghi chú nội dung xử lý.
* Ghi nhận các hoạt động liên quan đến quá trình xử lý.

### 4. Request Additional Information

Nhân viên có thể yêu cầu sinh viên cung cấp thêm thông tin hoặc tài liệu khi chưa đủ thông tin để xử lý yêu cầu.

Khi yêu cầu được gửi, hệ thống cập nhật trạng thái phù hợp để sinh viên biết cần bổ sung thông tin trước khi quá trình xử lý tiếp tục.

### 5. Transfer Request

Nhân viên có thể chuyển yêu cầu sang nhân viên hoặc phòng ban khác khi yêu cầu không thuộc trách nhiệm xử lý của mình.

Khi chuyển yêu cầu, hệ thống phải giữ lại các thông tin, tài liệu đính kèm và lịch sử trao đổi của yêu cầu.

### 6. Resolve and Close Request

Nhân viên có thể hoàn tất xử lý yêu cầu và cập nhật kết quả xử lý.

Sau khi yêu cầu được giải quyết, nhân viên có thể cập nhật yêu cầu sang trạng thái hoàn thành và đóng yêu cầu theo quy trình của hệ thống.

## Related Workflows

* [WF-02 – Classify and Assign](../../04-workflows/WF-02-classify-and-assign.md)
* [WF-03 – Process Request](../../04-workflows/WF-03-process-request.md)
* [WF-04 – Request Additional Information](../../04-workflows/WF-04-request-additional-information.md)
* [WF-05 – Transfer Request](../../04-workflows/WF-05-transfer-request.md)
* [WF-06 – Resolve and Close](../../04-workflows/WF-06-resolve-and-close.md)

## Related Functional Requirements

* [FR-St1 – Queue Management](../../05-requirements/functional-requirements.md#fr-st1-quản-lý-hàng-đợi)
* [FR-St2 – Processing & Escalation](../../05-requirements/functional-requirements.md#fr-st2-xử-lý-ghi-log-và-chuyển-cấp-yêu-cầu)
