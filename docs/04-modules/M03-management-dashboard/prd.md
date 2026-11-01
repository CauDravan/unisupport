# M03 – Management Dashboard

## Purpose

Dashboard dành cho Management để **theo dõi tình hình xử lý yêu cầu hỗ trợ, phát hiện các vấn đề cần chú ý và đánh giá hiệu quả hoạt động hỗ trợ**.

## Users

* Management

## Main capabilities

### 1. Monitor Request Overview

Management có thể xem tổng quan tình hình yêu cầu hỗ trợ trong hệ thống.

Dashboard hiển thị các thông tin chính:

* Số lượng yêu cầu mới.
* Số lượng yêu cầu đang xử lý.
* Số lượng yêu cầu quá hạn.
* Tình trạng xử lý của các yêu cầu.

### 2. Monitor Overdue Requests

Management có thể theo dõi các yêu cầu đã vượt quá thời gian xử lý dự kiến.

Hệ thống phải:

* Xác định các yêu cầu đã quá hạn dựa trên thời gian xử lý được quy định.
* Hiển thị cảnh báo rõ ràng đối với các yêu cầu quá hạn.
* Cho phép Management nhận biết các yêu cầu cần được chú ý.

### 3. View Performance Reports

Management có thể xem các báo cáo giúp đánh giá hiệu quả xử lý yêu cầu của các phòng ban.

Báo cáo bao gồm:

* Thời gian xử lý trung bình theo từng phòng ban.
* Khối lượng yêu cầu được xử lý.
* Tình hình xử lý yêu cầu theo trạng thái.

### 4. Analyze Common Request Types

Management có thể xem thống kê về các loại yêu cầu phổ biến để xác định những vấn đề thường xuyên phát sinh.

Hệ thống hiển thị:

* Các loại yêu cầu phổ biến.
* Số lượng hoặc tỷ lệ của từng loại yêu cầu.
* So sánh mức độ phổ biến giữa các loại yêu cầu.

### 5. View Student Feedback

Management có thể xem dữ liệu phản hồi của Student sau khi yêu cầu được hoàn thành.

Dữ liệu phản hồi được sử dụng để:

* Theo dõi mức độ hài lòng của Student.
* Đánh giá chất lượng hỗ trợ.
* Hỗ trợ việc xem xét và cải thiện hoạt động hỗ trợ.

## Related Functional Requirements

* [FR-M1 – Request Monitoring & Overdue Alerts](../../05-requirements/functional-requirements.md#fr-m1-request-monitoring-and-overdue-alerts)
* [FR-M2 – Performance & Reporting](../../05-requirements/functional-requirements.md#fr-m2-performance-and-reporting)
