# Project Constraints

## 1. Purpose

Tài liệu này ghi nhận các giới hạn được đề xuất hoặc cần tuân thủ trong quá trình lập kế hoạch, thiết kế, xây dựng prototype, kiểm thử và bàn giao UniSupport. Các constraint có nguồn xác định được phân biệt với các giới hạn đang được đề xuất trong bối cảnh simulated client để tránh thể hiện chúng như những quyết định đã được Aurora University xác nhận.

## 2. Project Schedule Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-01 | Dự án được lập kế hoạch trong thời gian 15 tuần. | Proposed planning baseline; subject to simulated client review. |
| PC-02 | Bốn Product Increment Milestones được lập kế hoạch theo các ngày mục tiêu trong Project Proposal và Master Plan. | Proposed schedule baseline; Master Plan Excel là nguồn lịch chi tiết. |
| PC-03 | Các thay đổi về lịch phải được đánh giá tác động đến milestone, dependencies và effort trước khi được chấp thuận. | Project planning and change-control constraint. |

## 3. Effort and Cost Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-04 | Planned effort cơ sở là 304 person-hours. | Current WBS/Master Plan baseline. |
| PC-05 | Contingency Reserve là 16 person-hours; tổng effort tối đa được đề xuất là 320 person-hours. | Proposed planning ceiling; usage of reserve requires review/approval and tracking. |
| PC-06 | Effort của các work items cần được estimate và theo dõi planned/actual. | Project control requirement. |
| PC-07 | Chi phí công cụ hoặc dịch vụ trả phí chưa được tính trong labour estimate; nếu cần sử dụng phải được đánh giá và phê duyệt riêng. | Pricing assumption A-01 and quotation basis. |
| PC-08 | Thay đổi scope hoặc effort ảnh hưởng đến giới hạn 320 person-hours phải được đánh giá và chấp thuận trước khi triển khai. | Proposed change-control rule. |

## 4. Prototype and Technical Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-09 | Prototype và testing sử dụng dữ liệu giả lập, không sử dụng dữ liệu sinh viên thật. | Confirmed for current planning in Project Assumptions AS-04. |
| PC-10 | Prototype được thiết kế để dùng thử trên desktop và mobile. | Proposed product compatibility constraint; acceptance scope to be defined in requirements. |
| PC-11 | Solution scope xem xét Student và Staff là các nhóm người dùng chính; Management và access/security needs được xác định trong requirements. | Project Proposal / current requirements baseline. |
| PC-12 | Giao diện và quy trình cần xem xét người dùng có mức độ thành thạo công nghệ khác nhau. | Proposed usability constraint. |
| PC-13 | Hỗ trợ tiếng Việt và tiếng Anh được xem xét trong prototype scope; mức độ hỗ trợ phải được xác định trong requirements. | Proposed constraint, subject to requirements validation. |

## 5. Scope and Governance Constraints

| ID | Constraint | Basis / Status |
|---|---|---|
| PC-14 | Prototype không được coi là sản phẩm production-ready hoặc triển khai chính thức toàn trường. | Project Proposal scope statement. |
| PC-15 | Role Administration (tự tạo hoặc thay đổi role) chưa được xác nhận là deliverable chính thức. | Project Proposal scope boundary. |
| PC-16 | Thay đổi scope, schedule, effort hoặc cost phải được ghi nhận, đánh giá tác động và xem xét phê duyệt trước khi thực hiện. | Project change-control approach. |
| PC-17 | Deliverables có thể được review và từ chối acceptance nếu không đáp ứng criteria đã thống nhất. | Simulated-client acceptance approach; detailed criteria referenced in requirements and Master Plan. |
| PC-18 | Tài liệu và artefacts bàn giao cần đủ rõ để nhóm tiếp nhận có thể hiểu, kiểm tra và tiếp tục phát triển. | Handover objective in Project Proposal. |

## 6. Constraint Management

- Project Manager theo dõi constraints và báo cáo các sai lệch hoặc nguy cơ ảnh hưởng baseline.
- Master Plan Excel là nguồn lịch, WBS, effort và milestone detail chính thức; các tài liệu khác chỉ tóm tắt hoặc tham chiếu.
- Các constraints có trạng thái proposed/subject to review không được trình bày như đã được Client xác nhận.
- Khi constraint thay đổi, nhóm đánh giá ảnh hưởng đến scope, schedule, effort, cost, requirements và deliverables, ghi nhận decision/change record, và chỉ thực hiện sau khi được xem xét phù hợp.
