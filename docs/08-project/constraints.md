# Project Constraints

## 1. Purpose

Tài liệu này ghi nhận các giới hạn và điều kiện cần xem xét trong quá trình lập kế hoạch, thiết kế, phát triển prototype, kiểm thử và bàn giao UniSupport.

Các constraints được phân biệt theo nguồn và trạng thái, bao gồm proposed planning baseline, team assumptions, current requirements baseline và project management constraints. Các nội dung chưa được simulated client xác nhận không được xem là quyết định chính thức của Aurora University.

## 2. Project Schedule Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-01 | Dự án được lập kế hoạch trong thời gian 15 tuần. | Proposed planning baseline; thời gian lập kế hoạch hiện tại trong Master Plan. |
| PC-02 | Dự án có 4 Product Increment Milestones (MS-01 đến MS-04), với các ngày mục tiêu được xác định trong Master Plan. | Proposed schedule baseline; Master Plan Excel là nguồn lịch chi tiết. |
| PC-03 | Các thay đổi về lịch phải được đánh giá tác động đến milestones, dependencies và effort trước khi được xem xét chấp thuận. | Project planning and change-control constraint. |

## 3. Effort and Cost Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-04 | Planned effort cơ sở của dự án là 304 person-hours. | Current WBS/Master Plan baseline. |
| PC-05 | Contingency Reserve là 16 person-hours; tổng effort dự kiến tối đa là 320 person-hours. | Proposed planning baseline; việc sử dụng reserve cần được review và tracking. |
| PC-06 | Effort của các work items phải được estimate và theo dõi planned/actual. | Project management and tracking approach. |
| PC-07 | Chi phí công cụ hoặc dịch vụ trả phí chưa được tính trong labour estimate; nếu cần sử dụng phải được đánh giá riêng. | Pricing assumption A-01 and quotation basis. |
| PC-08 | Các thay đổi scope hoặc effort ảnh hưởng đến giới hạn effort hiện tại phải được đánh giá và xem xét chấp thuận trước khi triển khai. | Proposed change-control constraint. |

## 4. Prototype and Technical Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-09 | Prototype và testing sử dụng dữ liệu giả lập, không sử dụng dữ liệu sinh viên thật. | Team assumption AS-04 for the current prototype scope. |
| PC-10 | Prototype được thiết kế để xem xét và dùng thử trên desktop và mobile. | Proposed product compatibility constraint; acceptance scope được xác định trong requirements. |
| PC-11 | Student và Staff là các nhóm người dùng chính trong phạm vi hiện tại; Management và các yêu cầu về access/security được xác định trong requirements baseline. | Current Project Proposal and requirements baseline. |
| PC-12 | Giao diện và quy trình cần xem xét người dùng có mức độ thành thạo công nghệ khác nhau. | Proposed usability constraint. |
| PC-13 | Prototype scope xem xét hỗ trợ tiếng Việt và tiếng Anh; mức độ hỗ trợ được xác định trong requirements. | Proposed product constraint; subject to requirements validation. |

## 5. Scope and Governance Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-14 | Prototype không được xem là sản phẩm production-ready hoặc hệ thống đã triển khai chính thức toàn trường. | Project Proposal scope boundary. |
| PC-15 | Role Administration (tự tạo hoặc thay đổi role) chưa được xác định là deliverable chính thức trong scope hiện tại. | Current Project Proposal scope boundary. |
| PC-16 | Thay đổi scope, schedule, effort hoặc cost phải được ghi nhận và đánh giá tác động trước khi thực hiện. | Project change-control approach. |
| PC-17 | Deliverables được review theo acceptance criteria đã xác định; các deliverables không đáp ứng criteria cần được xử lý trước khi được chấp nhận. | Simulated-client acceptance approach; detailed criteria referenced in requirements and Master Plan. |
| PC-18 | Tài liệu và artefacts bàn giao cần đủ rõ để người tiếp nhận có thể hiểu, kiểm tra và tiếp tục phát triển prototype. | Project handover objective in Project Proposal. |

## 6. Constraint Management

- Project Manager theo dõi constraints và báo cáo các sai lệch hoặc nguy cơ ảnh hưởng đến project baseline.
- Master Plan Excel là nguồn chính cho lịch, WBS, effort và milestone details; các tài liệu khác chỉ tóm tắt hoặc tham chiếu những nội dung này.
- Các constraints có trạng thái proposed hoặc subject to review không được trình bày như đã được simulated client xác nhận.
- Team assumptions được ghi nhận trong `assumptions.md`; các vấn đề cần xác nhận được ghi nhận trong `open-questions.md`.
- Khi constraint thay đổi, nhóm đánh giá tác động đến scope, schedule, effort, cost, requirements và deliverables; thay đổi được ghi nhận và xem xét theo project change-control approach trước khi thực hiện.
