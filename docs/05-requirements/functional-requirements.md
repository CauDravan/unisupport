# Functional Requirements

Các yêu cầu chức năng mô tả những chức năng và hành vi mà hệ thống UniSupport
cần cung cấp cho từng nhóm người dùng.

---

## 1. Student Portal

<a id="fr-s1-request-submission"></a>
### FR-S1 – Request Submission

**Description**

Sinh viên có thể gửi yêu cầu hỗ trợ thông qua hệ thống bằng cách cung cấp
thông tin cần thiết, lựa chọn loại yêu cầu và đính kèm tài liệu liên quan nếu cần.

**Requirements**

- Hệ thống phải yêu cầu các thông tin bắt buộc trước khi tạo Request.
- Student có thể lựa chọn Request Type từ danh sách được hệ thống cung cấp.
- Student có thể đính kèm các tệp liên quan.
- Hệ thống tạo Request ID sau khi Request được gửi thành công.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Workflow: [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)

---

<a id="fr-s2-request-tracking"></a>
### FR-S2 – Request Tracking

**Description**

Sinh viên có thể theo dõi trạng thái và lịch sử xử lý của các yêu cầu đã gửi.

**Requirements**

- Hệ thống hiển thị trạng thái hiện tại của Request.
- Hệ thống hiển thị các mốc cập nhật liên quan đến Request.
- Student chỉ có thể xem các Request thuộc tài khoản của mình.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Workflow: [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)
- Workflow: [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)

---

<a id="fr-s3-additional-information-feedback"></a>
### FR-S3 – Additional Information & Feedback

**Description**

Sinh viên có thể cung cấp thông tin bổ sung khi nhân viên yêu cầu và gửi
feedback sau khi yêu cầu được xử lý.

**Requirements**

- Student được thông báo khi Request chuyển sang trạng thái yêu cầu bổ sung thông tin.
- Student có thể cung cấp thông tin bổ sung cho Request.
- Student có thể gửi Feedback sau khi Request được giải quyết.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Workflow: [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- Workflow: [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)

---

## 2. Staff Workspace

<a id="fr-st1-queue-management"></a>
### FR-St1 – Queue Management

**Description**

Nhân viên có thể xem và quản lý các Request được chuyển đến bộ phận của mình
trên một hàng đợi tập trung.

**Requirements**

- Staff có thể xem các Request thuộc phạm vi được phân công.
- Staff có thể lọc Request theo Status và Priority.
- Hệ thống hiển thị thời gian chờ của Request.

**Related**

- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Workflow: [WF-02 – Classify and Assign](../04-workflows/WF-02-classify-and-assign.md)

---

<a id="fr-st2-processing-and-escalation"></a>
### FR-St2 – Request Processing & Escalation

**Description**

Nhân viên có thể xử lý Request, cập nhật tiến độ, yêu cầu bổ sung thông tin
và chuyển Request sang bộ phận khác khi cần.

**Requirements**

- Staff có thể cập nhật Status của Request.
- Staff có thể ghi nhận nội dung xử lý.
- Staff có thể yêu cầu Student cung cấp thêm thông tin.
- Staff có thể Transfer Request sang bộ phận khác.
- Hệ thống lưu lại các hoạt động xử lý cần thiết.

**Related**

- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Workflow: [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)
- Workflow: [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- Workflow: [WF-05 – Transfer Request](../04-workflows/WF-05-transfer-request.md)
- Workflow: [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)

---

## 3. Management Dashboard

<a id="fr-m1-request-monitoring-and-overdue-alerts"></a>
### FR-M1 – Request Monitoring & Overdue Alerts

**Description**

Management có thể theo dõi tình hình xử lý Request và nhận biết các Request
đang có nguy cơ hoặc đã vượt quá thời gian xử lý dự kiến.

**Requirements**

- Hệ thống hiển thị số liệu tổng quan về Request.
- Management có thể theo dõi các Request đang xử lý và quá hạn.
- Hệ thống hiển thị cảnh báo đối với các Request vượt quá thời gian xử lý dự kiến.

**Related**

- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)

---

<a id="fr-m2-performance-and-reporting"></a>
### FR-M2 – Performance & Reporting

**Description**

Management có thể xem các báo cáo và số liệu tổng hợp để đánh giá hiệu quả
xử lý yêu cầu hỗ trợ.

**Requirements**

- Hệ thống cung cấp số liệu về thời gian xử lý Request.
- Hệ thống cung cấp thống kê theo Request Type.
- Hệ thống cung cấp các số liệu phù hợp để đánh giá chất lượng dịch vụ.

**Related**

- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)