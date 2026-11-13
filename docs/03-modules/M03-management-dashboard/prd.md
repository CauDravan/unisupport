# M03 – Management Dashboard

## 1. Purpose

Management Dashboard là module dành cho Management để theo dõi tình hình tiếp nhận và xử lý các Request trong hệ thống UniSupport.

Module cung cấp số liệu tổng quan, cảnh báo Request quá hạn và các báo cáo về hiệu quả xử lý, khối lượng công việc theo Department, Request Type phổ biến và Feedback từ Student.

Thông qua các thông tin này, Management có thể nhận biết những vấn đề cần chú ý, đánh giá chất lượng hoạt động hỗ trợ và có cơ sở xem xét việc cải thiện dịch vụ.

## 2. Users

### Primary User

- **Management:** Người theo dõi tình hình hoạt động, xem báo cáo và đánh giá hiệu quả hỗ trợ sinh viên.

## 3. Main Capabilities

### 3.1 Monitor Request Overview

Management có thể xem tổng quan tình hình Request trong hệ thống thông qua Dashboard.

Dashboard hiển thị các thông tin chính:

- Số lượng Request mới.
- Số lượng Request đang xử lý.
- Danh sách hoặc số lượng Request quá hạn.
- Tình hình Request theo Status.

Hệ thống tổng hợp dữ liệu từ các Request đã được ghi nhận và hiển thị số liệu phản ánh trạng thái tại thời điểm Management truy vấn.

**Expected Result:** Management có thể nắm được tình hình tiếp nhận và xử lý Request, đồng thời nhận biết những Request cần được theo dõi.

### 3.2 Monitor Overdue Requests

Management có thể theo dõi các Request đã vượt quá thời gian xử lý mục tiêu được cấu hình trong hệ thống.

Hệ thống hỗ trợ:

- Xác định Request quá hạn dựa trên thời gian xử lý mục tiêu.
- Hiển thị danh sách Request quá hạn.
- Hiển thị cảnh báo đối với các Request vượt quá thời gian xử lý mục tiêu.
- Cho phép Management xem thông tin chi tiết của Request trong phạm vi quyền truy cập.

**Expected Result:** Management có thể nhận biết Request đang quá hạn và xem thông tin liên quan để theo dõi tình hình xử lý.

### 3.3 View Performance Reports

Management có thể xem các báo cáo tổng hợp để đánh giá hiệu quả xử lý Request và khối lượng công việc của các Department.

Báo cáo bao gồm:

- Thời gian xử lý Request trung bình.
- Số lượng Request được xử lý.
- Khối lượng Request theo từng Department.
- Tình hình xử lý Request theo Status.

Các số liệu được tổng hợp từ dữ liệu Request và hoạt động xử lý đã được ghi nhận trong hệ thống.

**Expected Result:** Management có cơ sở đánh giá hiệu quả xử lý và nhận biết sự khác biệt về khối lượng công việc giữa các Department.

### 3.4 Analyze Common Request Types

Management có thể xem thống kê về các Request Type phổ biến nhằm nhận biết những vấn đề thường xuyên phát sinh từ Student.

Hệ thống hiển thị:

- Danh sách các Request Type đã được phân loại.
- Số lượng Request thuộc từng Request Type.
- Tỷ lệ của từng Request Type trong tổng số Request được thống kê.

Dữ liệu thống kê được tổng hợp dựa trên Request Type đã được ghi nhận trong quá trình phân loại Request.

**Expected Result:** Management có thể xác định những nhóm vấn đề phổ biến mà Student thường gặp và sử dụng thông tin này để xem xét việc cải thiện hoạt động hỗ trợ.

### 3.5 View Student Feedback

Management có thể xem Feedback do Student gửi sau khi Request được xử lý.

Thông tin Feedback được sử dụng để:

- Theo dõi Rating của Student đối với kết quả hỗ trợ.
- Xem Comment do Student cung cấp nếu có.
- Đánh giá mức độ hài lòng của Student.
- Hỗ trợ việc xem xét và cải thiện chất lượng dịch vụ hỗ trợ.

Feedback được liên kết với Request tương ứng để Management có thể xem xét trong bối cảnh kết quả xử lý.

**Expected Result:** Management có thể sử dụng Feedback làm cơ sở đánh giá chất lượng hỗ trợ và nhận biết những điểm cần cải thiện.

## 4. Related Functional Requirements

- [FR-MGT-01 – Request Monitoring and Overdue Alerts](../../05-requirements/functional-requirements.md#fr-mgt-01--request-monitoring-and-overdue-alerts)
- [FR-MGT-02 – Performance and Management Reporting](../../05-requirements/functional-requirements.md#fr-mgt-02--performance-and-management-reporting)

## 5. Related Acceptance Criteria

- [AC-11 – Management mở Management Dashboard](../../06-acceptance/acceptance-criteria.md#ac-11)
- [AC-14 – Student gửi Feedback sau khi Request được xử lý](../../06-acceptance/acceptance-criteria.md#ac-14)

## 6. Related Workflows

M03 không có Workflow riêng. Các Functional Requirements của module được kiểm chứng thông qua các hoạt động và dữ liệu được ghi nhận trong hệ thống.

- **WF-07 – Feedback:** Cung cấp dữ liệu Feedback của Student để phục vụ việc đánh giá chất lượng dịch vụ theo FR-MGT-02.
- **WF-02 đến WF-06:** Cung cấp dữ liệu về phân loại, phân công và xử lý Request để phục vụ Request Monitoring và Performance Reporting.

## 7. Related Modules

- **M01 – Student Portal:** Student gửi Request, theo dõi tiến độ và cung cấp Feedback. Những dữ liệu này được sử dụng trong Management Dashboard.
- **M02 – Staff Workspace:** Staff phân loại, phân công và xử lý Request. Các thông tin xử lý được sử dụng để tổng hợp số liệu và báo cáo.
- **M04 – Security and Access:** Kiểm soát quyền truy cập của Management đối với Dashboard và dữ liệu được tổng hợp.

## 8. Scope Notes

- Dashboard chỉ tổng hợp dữ liệu Request và hoạt động đã được ghi nhận trong hệ thống.
- Request được xác định là quá hạn dựa trên thời gian xử lý mục tiêu được cấu hình; module không tự đặt ra thời hạn xử lý mới.
- Management chỉ được xem dữ liệu thuộc phạm vi quyền truy cập được cấp.
- Báo cáo không thể tính toán chính xác khi dữ liệu đầu vào cần thiết chưa đầy đủ; hệ thống cần hiển thị thông báo phù hợp.
- Student Feedback là nguồn dữ liệu phục vụ đánh giá chất lượng dịch vụ, không đồng nghĩa với việc hệ thống tự động đưa ra quyết định đánh giá hiệu suất nhân viên.