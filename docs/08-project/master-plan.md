# Master Plan

## 1. Purpose

Master Plan xác định kế hoạch tổng thể cho dự án UniSupport, bao gồm phạm vi công việc, lịch trình, nguồn lực, các mốc bàn giao và việc quản lý thay đổi.

Tài liệu này cung cấp cái nhìn tổng quan về cách nhóm tổ chức và kiểm soát dự án trong suốt 15 tuần thực hiện.

File `master-plan.xlsx` là tài liệu quản lý kế hoạch chi tiết và là nguồn dữ liệu chính thức (Single Source of Truth) cho lịch trình, Work Breakdown Structure (WBS), Milestones, Resources và Change Log.

## 2. Planning Overview

Dự án UniSupport được lập kế hoạch với các thông tin chính sau:

| Item | Description |
|---|---|
| Project Name | UniSupport – Student Support Management System |
| Project Client | Aurora University (Simulated Client) |
| Project Sponsor | Director of Student Services |
| Project Duration | 15 weeks |
| Planned Start Date | 16/11/2026 (Tentative) |
| Planned End Date | 26/02/2027 |
| Maximum Planned Effort | 320 person-hours |
| Project Team | 4 members |

Ngày bắt đầu hiện là giả định tạm thời và cần được nhóm xác nhận trước khi chốt Project Baseline.

## 3. Master Plan Structure

File `master-plan.xlsx` bao gồm 5 sheets, mỗi sheet đảm nhiệm một phần quản lý dự án:

| Sheet | Purpose |
|---|---|
| Milestones | Xác định các mốc bàn giao, deliverables và điều kiện nghiệm thu. |
| WBS | Phân chia công việc thành các task, xác định effort, thời gian và dependencies. |
| Resources | Theo dõi phân công trách nhiệm và nguồn lực của từng thành viên. |
| Gantt | Trực quan hóa lịch trình dự án dựa trên ngày bắt đầu và kết thúc trong WBS. |
| Change Log | Ghi nhận các thay đổi đối với kế hoạch, lý do và trạng thái phê duyệt. |

## 4. Schedule and Milestone Management

Dự án được chia thành 4 Milestones chính:

| Milestone | Deliverable | Planned Completion |
|---|---|---|
| MS-01 | Student Request Submission & Tracking | 15/01/2027 |
| MS-02 | Staff Request Classification & Processing | 29/01/2027 |
| MS-03 | Request Transfer, Resolution & Feedback | 12/02/2027 |
| MS-04 | Management Dashboard, Security & Handover | 26/02/2027 |

Mỗi Milestone đại diện cho một nhóm chức năng có thể được kiểm tra và đánh giá bởi client.

Việc hoàn thành Milestone phải dựa trên các deliverables và acceptance criteria đã xác định, không chỉ dựa trên ngày kết thúc công việc.

Lịch trình được quản lý theo các nguyên tắc:

- WBS là nơi xác định công việc, effort và dependencies.
- Gantt được sử dụng để theo dõi tiến độ theo tuần.
- Milestones xác định các thời điểm bàn giao và nghiệm thu.
- Các Milestone trên GitHub phải sử dụng cùng mã MS-xx và ngày kết thúc với Master Plan Excel.
- Planned effort và actual effort được theo dõi để kiểm soát nguồn lực.

## 5. Change Control

Mọi thay đổi ảnh hưởng đến phạm vi, lịch trình, effort, nguồn lực hoặc deliverables cần được ghi nhận và xem xét trước khi cập nhật kế hoạch.

Quy trình quản lý thay đổi được thực hiện như sau:

1. Ghi nhận yêu cầu thay đổi và lý do.
2. Đánh giá ảnh hưởng đến scope, schedule, effort và resources.
3. Xác định người có trách nhiệm xem xét và phê duyệt.
4. Cập nhật kế hoạch sau khi thay đổi được chấp thuận.
5. Ghi lại nội dung và trạng thái thay đổi trong sheet Change Log.
6. Đồng bộ những nội dung liên quan trên GitHub và các tài liệu dự án.

Các phiên bản kế hoạch trước đó cần được lưu lại để nhóm có thể theo dõi lịch sử thay đổi và đối chiếu khi cần thiết.

## 6. Related Documents

Các tài liệu liên quan đến Master Plan:

- [Master Plan Excel](master-plan.xlsx)
- [Work Breakdown Structure](wbs.md)
- [Risk Register](risk-register.md)
- [RACI Matrix](raci-matrix.md)
- [Team Charter](team-charter.md)
- [Project Proposal](project_proposal.docx)