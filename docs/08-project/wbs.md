# Work Breakdown Structure (WBS)

## 1. Purpose

Work Breakdown Structure (WBS) phân rã công việc của UniSupport thành các work packages để xác định phạm vi công việc, effort, dependencies, trách nhiệm và kết quả cần bàn giao.

## 2. Official WBS Source

**`docs/08-project/master-plan.xlsx`, sheet `WBS`, là nguồn chính thức (Single Source of Truth)** cho WBS IDs, work packages, milestone mapping, effort, schedule, dependencies và các thông tin chi tiết phục vụ lập kế hoạch.

Tài liệu Markdown này chỉ giải thích cấu trúc WBS và không duy trì một bản bảng WBS chi tiết thứ hai. Khi có thay đổi được phê duyệt, cập nhật Excel trước; nội dung mô tả tại đây chỉ được chỉnh nếu cấu trúc hoặc nguyên tắc quản lý WBS thay đổi.

## 3. WBS Structure

Sheet WBS trong Master Plan Excel được tổ chức thành các nhóm công việc:

1. Project Initiation & Analysis.
2. Requirements & Solution Design.
3. MS-01 – Student Request Submission & Tracking.
4. MS-02 – Staff Request Classification & Processing.
5. MS-03 – Request Transfer, Resolution & Feedback.
6. MS-04 – Management Dashboard, Security & Handover.
7. Project Management & Control.
8. Documentation & Handover.
9. Contingency Reserve.

Các nhóm 3–6 được triển khai theo Product Increment Milestones, nhằm kiểm tra và bàn giao từng phần prototype thay vì chờ toàn bộ hệ thống hoàn thành.

## 4. WBS and Project Tracking

- **Master Plan Excel:** nguồn chính thức cho WBS, schedule, dependencies, effort, milestones, resource allocation và Change Log.
- **GitHub Issues:** theo dõi work items, owner, deadline, status, liên kết WBS/FR/TS/MS và evidence khi có.
- **GitHub Milestones:** sử dụng MS-01 đến MS-04 và ngày mục tiêu tương ứng với Master Plan Excel.
- **RACI Matrix:** xác định trách nhiệm ở cấp hoạt động; không thay thế việc assign task cụ thể.
- **Risk Register:** theo dõi các rủi ro có thể ảnh hưởng đến công việc, schedule, effort và deliverables.

## 5. Change Management

Khi thay đổi scope, requirements, schedule, effort, dependencies hoặc resources:

1. Ghi nhận Change Request.
2. Đánh giá ảnh hưởng.
3. Xem xét và phê duyệt theo Project Governance.
4. Cập nhật Master Plan Excel sau khi được chấp thuận.
5. Đồng bộ GitHub Issues và các tài liệu bị ảnh hưởng.
6. Ghi nhận lịch sử trong Change Log.

**Related documents:** `master-plan.xlsx`, `master-plan.md`, `raci-matrix.md`, `risk-register.md`, `team-charter.md`, `project-proposal.md`.
