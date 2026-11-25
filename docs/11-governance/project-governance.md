# Project Governance

## 1. Purpose

Tài liệu này quy định cách nhóm UniSupport theo dõi, báo cáo và kiểm soát dự án; cách ghi nhận vấn đề/rủi ro, thực hiện escalation và xử lý Change Request (CR). Mục tiêu là bảo đảm các quyết định ảnh hưởng đến Product Scope, schedule, effort, resources và deliverables được xem xét, phê duyệt và cập nhật nhất quán.

UniSupport được thực hiện trong bối cảnh **Simulated Client**. Các vai trò phê duyệt trong tài liệu mô tả cơ chế quản trị dự án mô phỏng, không có nghĩa Aurora University hoặc Director of Student Services đã chính thức xác nhận các quyết định này.

## 2. Governance Principles

- **One schedule baseline:** `docs/08-project/master-plan.xlsx` là nguồn dữ liệu chính thức cho Milestones, WBS, Resources, Gantt và Change Log.
- **Traceable work:** GitHub Issues được sử dụng để theo dõi task cụ thể; GitHub Milestones phải đồng bộ mã MS-xx và ngày với Master Plan.
- **Evidence-based decisions:** Báo cáo trạng thái và quyết định cần dựa trên deliverables, Acceptance Criteria, test evidence, actual effort và thông tin rủi ro có thể kiểm tra.
- **Controlled changes:** Không tự ý thay đổi baseline về scope, schedule, effort, resources hoặc deliverables trước khi có phê duyệt phù hợp.
- **Clear accountability:** Mỗi task có người phụ trách chính; trách nhiệm ở cấp hoạt động được tham chiếu từ [RACI Matrix](../08-project/raci-matrix.md).

## 3. Governance Roles and Responsibilities

| Role | Governance Responsibilities |
|---|---|
| Project Manager (PM) | Điều phối hoạt động quản lý dự án; theo dõi Master Plan và GitHub; tổng hợp tiến độ, effort, issue và risk; tổ chức review; điều phối impact assessment cho CR; duy trì Change Log và thông báo các quyết định đã được xác nhận. |
| Business Analyst (BA) | Theo dõi tính nhất quán của Product Scope, PRD, Functional Requirements, Workflows, Acceptance Criteria và Test Scenarios; phân tích tác động nghiệp vụ của Feedback/CR; cung cấp bằng chứng xác nhận yêu cầu. |
| Front-end Developer (FE) | Báo cáo tiến độ và trở ngại của công việc giao diện; cung cấp thông tin về tác động kỹ thuật, effort và kiểm thử liên quan đến phần Front-end. |
| Back-end Developer (BE) | Báo cáo tiến độ và trở ngại của công việc xử lý nghiệp vụ/dữ liệu; cung cấp thông tin về tác động kỹ thuật, effort, quyền truy cập và kiểm thử liên quan đến Back-end. |
| Project Sponsor / Simulated Client | Trong cơ chế dự án mô phỏng, xem xét và chấp thuận hoặc từ chối các CR làm thay đổi baseline hoặc cam kết bàn giao. Vai trò này không được xem là quyết định chính thức của Aurora University. |

Phân công chi tiết giữa PM, BA, FE và BE tuân theo [RACI Matrix](../08-project/raci-matrix.md). Project Manager điều phối quy trình và đưa ra khuyến nghị; việc điều phối này không thay thế quyền chấp thuận CR ảnh hưởng đến baseline của Project Sponsor / Simulated Client.

## 4. Progress Monitoring and Reporting

### 4.1 Sources of Progress Information

PM tổng hợp thông tin từ các nguồn sau:

| Source | Information to Monitor | Responsible Role |
|---|---|---|
| `master-plan.xlsx` – WBS and Gantt | Planned dates, dependencies, planned effort và actual effort nếu đã ghi nhận. | PM; task owner cập nhật thông tin phần việc. |
| `master-plan.xlsx` – Milestones | Deliverables, planned completion và Acceptance Criteria của MS-01 đến MS-04. | PM phối hợp BA và người thực hiện deliverable. |
| GitHub Issues / Project Board | Owner, deadline, trạng thái, liên kết FR/TS/MS-xx và bằng chứng hoàn thành. | Người được giao task cập nhật; PM theo dõi tổng thể. |
| Risk Register | Risk, owner, impact, response và trạng thái. | PM phối hợp Risk Owner. |
| Test Scenarios / Test Results | Kết quả kiểm thử, defect và bằng chứng nghiệm thu. | BA điều phối xác nhận; FE/BE hỗ trợ kiểm thử kỹ thuật. |

### 4.2 Reporting Cycle (Chu kỳ báo cáo)

| Reporting Activity | Responsible | Recipient | Frequency | Report Content |
|---|---|---|---|---|
| **Task-level Update** | Task Owner | PM | Khi trạng thái task thay đổi, gặp blocker hoặc có nguy cơ trễ tiến độ | Công việc đã hoàn thành, công việc còn lại, trở ngại, ảnh hưởng và hành động tiếp theo |
| **Internal Project Report** | PM | Project Team | Hằng tuần | Tiến độ tổng thể, trạng thái milestone, planned vs. actual effort nếu có, vấn đề, rủi ro và công việc sắp tới |
| **Client Progress Report** | PM | Project Sponsor / Simulated Client | Hằng tuần | Tiến độ milestone, deliverables đã hoàn thành, công việc còn lại, rủi ro, vấn đề, quyết định cần client đưa ra và kỳ báo cáo tiếp theo |
| **Milestone Review** | PM, BA and relevant Task Owners | Project Team and Project Sponsor / Simulated Client | Cuối mỗi milestone | Deliverables, tiêu chí nghiệm thu, bằng chứng kiểm thử, vấn đề còn tồn tại và đề xuất hoàn thành milestone |

- Task Owners phải cập nhật GitHub Issues khi trạng thái thay đổi, phát sinh blocker hoặc deadline có nguy cơ bị ảnh hưởng.

- PM tổng hợp thông tin từ Master Plan, GitHub Issues, Risk Register và Test Results để chuẩn bị báo cáo nội bộ và báo cáo client hằng tuần.

- Client Progress Report được gửi cho Project Sponsor / Simulated Client qua kênh liên lạc đã thống nhất.

- Cuối mỗi milestone, PM phối hợp với BA và các Task Owner liên quan để kiểm tra deliverables dựa trên Acceptance Criteria và bằng chứng kiểm thử hiện có.

- Các báo cáo và quyết định quan trọng được lưu trong project repository để phục vụ theo dõi dự án và bàn giao.

### 4.3 Minimum Progress Report

Báo cáo tiến độ tối thiểu nên có:

1. Reporting date và kỳ báo cáo.
2. Milestone/WBS task đang theo dõi và trạng thái hiện tại.
3. Planned progress so với actual progress, nếu dữ liệu đã được cập nhật.
4. Planned effort so với actual effort, nếu đã có số liệu.
5. Deliverables/Acceptance Criteria đã hoàn thành và evidence tương ứng.
6. Open issues, risks, blockers và tác động dự kiến.
7. Việc cần quyết định hoặc hỗ trợ, người phụ trách và thời hạn tiếp theo.

Không tự kết luận một Milestone đạt tiến độ hoặc được nghiệm thu nếu chưa có dữ liệu và bằng chứng tương ứng.

## 5. Monitoring Indicators and Escalation Triggers

Các điều kiện dưới đây được dùng để nhận biết tình huống cần PM xem xét. Đây là **escalation triggers theo kế hoạch dự án**, không phải SLA vận hành của UniSupport.

| Trigger | Required Action | Escalation Path |
|---|---|---|
| Task có nguy cơ trễ deadline hoặc dependency bị ảnh hưởng | Task owner cập nhật nguyên nhân, ảnh hưởng và phương án khắc phục trên GitHub Issue; thông báo PM. | Task Owner → PM → nhóm liên quan. |
| Có nguy cơ ảnh hưởng ngày hoàn thành MS-01, MS-02, MS-03 hoặc MS-04 | PM đánh giá tác động đến WBS/Gantt, deliverables, dependencies và nguồn lực; đề xuất phương án cho nhóm. | PM → nhóm dự án; nếu cần thay đổi baseline thì trình Project Sponsor / Simulated Client. |
| Effort dự kiến vượt giới hạn tối đa 320 person-hours hoặc cần thay đổi nguồn lực | PM cùng task owner rà soát actual/remaining effort và phương án ưu tiên hoặc điều chỉnh; không tự tăng giới hạn. | PM → nhóm → Project Sponsor / Simulated Client nếu thay đổi baseline/cam kết. |
| Đề xuất làm thay đổi Product Scope, yêu cầu đã thống nhất hoặc deliverable | Ghi nhận CR, phân tích tác động và chờ quyết định trước khi triển khai thay đổi. | PM điều phối → Project Sponsor / Simulated Client xem xét phê duyệt. |
| Phát hiện lỗi nghiêm trọng liên quan đến dữ liệu, quyền truy cập hoặc luồng nghiệp vụ cốt lõi | Ghi nhận Bug, đánh giá Severity theo Quality Plan, tạm dừng việc đánh dấu chức năng liên quan là hoàn thành cho đến khi có kết quả xử lý/đánh giá. | Người phát hiện → PM và BA → FE/BE liên quan; báo Project Sponsor / Simulated Client nếu ảnh hưởng nghiệm thu hoặc baseline. |
| Thành viên không thể tiếp tục task hoặc vắng mặt ảnh hưởng đến bàn giao | Thành viên thông báo sớm khi có thể; PM rà soát trạng thái, tài liệu bàn giao và phân công hỗ trợ phù hợp. | Thành viên/Task Owner → PM → nhóm. |
| Nhóm không thống nhất được quyết định hoặc phương án xử lý | PM ghi nhận các lựa chọn, tác động và điểm chưa thống nhất; đưa ra thảo luận theo Team Charter. | PM → nhóm; vấn đề liên quan baseline được trình Project Sponsor / Simulated Client. |

### 5.1 Escalation Record

Khi escalation, bản ghi cần có:

- Issue/Risk ID hoặc GitHub Issue liên quan.
- Ngày phát hiện và người báo cáo.
- Mô tả tình trạng và nguyên nhân đã biết.
- Ảnh hưởng đến scope, schedule, effort, resources, quality hoặc milestone.
- Phương án xử lý được đề xuất và các lựa chọn khác nếu có.
- Người cần đưa ra quyết định, quyết định cuối cùng và ngày quyết định.
- Owner, action tiếp theo, deadline và trạng thái theo dõi.

## 6. Change Control and Approval Authority

### 6.1 Changes Requiring Formal Review

CR cần được ghi nhận và đánh giá khi có khả năng thay đổi một hoặc nhiều nội dung sau:

- Product Scope hoặc Functional Requirements đã thống nhất.
- Milestone, planned completion date, WBS dependency hoặc schedule baseline.
- Effort, giới hạn 320 person-hours hoặc phân bổ resources.
- Deliverables hoặc Acceptance Criteria đã cam kết.

Lỗi khiến prototype không đáp ứng yêu cầu đã thống nhất được quản lý như Bug theo Feedback Process và Quality Plan; không tự động xem mọi Bug là CR. Nếu cách sửa Bug làm thay đổi baseline hoặc bổ sung phạm vi mới, phần thay đổi đó phải được xem xét như CR.

### 6.2 Change Request Workflow

1. **Submit:** Người đề xuất tạo CR record/GitHub Issue, mô tả nội dung thay đổi, lý do, lợi ích và module/workflow liên quan.
2. **Log:** PM ghi nhận CR trong Change Log của `master-plan.xlsx` và theo dõi trạng thái.
3. **Impact Assessment:** PM phối hợp BA, FE, BE và task owner đánh giá ảnh hưởng đến scope, FR/NFR, workflow, Acceptance Criteria, test scenarios, schedule, dependencies, effort, resources và quotation khi phù hợp.
4. **Recommendation:** Nhóm đưa ra khuyến nghị Accept, Reject hoặc Defer, kèm lý do và ảnh hưởng.
5. **Approval:** CR làm thay đổi baseline hoặc cam kết bàn giao phải được Project Sponsor / Simulated Client xem xét và chấp thuận trước khi cập nhật baseline. PM không tự phê duyệt thay đổi loại này. Các điều chỉnh thực hiện trong phạm vi task đã được giao, không làm thay đổi baseline, được PM điều phối và ghi nhận theo Team Charter.
6. **Update:** Sau khi được chấp thuận, PM cập nhật Change Log và phối hợp cập nhật các tài liệu bị ảnh hưởng, Master Plan, Product Backlog và GitHub Milestones/Issues.
7. **Verify and Close:** BA và người thực hiện kiểm tra nội dung đã cập nhật; PM đóng CR khi có quyết định và bằng chứng đồng bộ phù hợp.

CR chưa được phê duyệt phải giữ trạng thái Pending/Deferred/Rejected tương ứng; không được đưa vào baseline hoặc mô tả như chức năng đã cam kết.

### 6.3 Change Decision Record

Mỗi quyết định CR cần ghi tối thiểu: CR ID, mô tả, người đề xuất, ngày nhận, impact assessment, khuyến nghị của nhóm, người phê duyệt, quyết định/ngày quyết định, lý do, tài liệu bị ảnh hưởng và trạng thái triển khai.

## 7. Governance Records and Repository Locations

| Record | Location | Purpose |
|---|---|---|
| Master Plan and Change Log | `docs/08-project/master-plan.xlsx` | Nguồn chính thức cho schedule, WBS, resources, milestones và lịch sử CR. |
| Project monitoring rules | `docs/11-governance/project-governance.md` | Quy định báo cáo, theo dõi, escalation và approval authority. |
| Task status and decisions | GitHub Issues / Project Board | Theo dõi owner, deadline, trạng thái, blocker và liên kết công việc. |
| Risk records | `docs/08-project/risk-register.md` | Theo dõi risk, owner và response. |
| Role responsibilities | `docs/08-project/raci-matrix.md` | Phân định R/A/C/I cho hoạt động dự án. |
| Team working agreement | `docs/08-project/team-charter.md` | Quy định phối hợp, cập nhật tiến độ, họp và làm việc nhóm. |
| Product feedback and CR intake | `docs/10-product-management/feedback-process.md` | Tiếp nhận, phân loại, đánh giá và theo dõi Feedback/CR. |

## 8. Open Decisions and Confirmation Required

Các mục sau đây vẫn chưa được xác nhận và cần đạt được sự đồng thuận trước khi được coi là các thông số cơ sở (baselines) của dự án:

1. **Escalation response time:** Hiện chưa có thời gian phản hồi cố định nào được xác nhận. Nhóm có thể thiết lập các hướng dẫn phản hồi nội bộ, nhưng những hướng dẫn này không được coi là Thỏa thuận mức dịch vụ (SLA) của Đại học Aurora.
2. **Named approver:** Vai trò phê duyệt được xác định là Nhà tài trợ dự án / Khách hàng giả định (theo giả định của dự án, vai trò này thuộc về Giám đốc Dịch vụ Sinh viên). Hiện chưa có cá nhân cụ thể nào được chỉ định hoặc có xác nhận chính thức từ phía khách hàng.
3. **Actual team assignment:** Cơ cấu dự kiến ​​bao gồm bốn vai trò (Quản lý dự án - PM, Chuyên viên phân tích nghiệp vụ - BA, Lập trình viên Front-end - FE và Lập trình viên Back-end - BE). Việc phân công thực tế và tình trạng sẵn sàng tham gia của các thành viên cần được xác nhận, đồng thời phải thống nhất với bảng phân bổ nguồn lực (Resources sheet) và danh sách người được phân công trên GitHub.

Quy trình giải quyết bất đồng nội bộ của nhóm được quy định trong Team Charter. Nhóm ưu tiên đạt được sự đồng thuận; nếu không thể đạt được sự đồng thuận đối với một vấn đề không ảnh hưởng đến các thông số cơ sở của dự án, Quản lý dự án (PM) sẽ đưa ra quyết định cuối cùng và ghi lại quyết định đó. Các thay đổi ảnh hưởng đến thông số cơ sở của dự án vẫn phải được sự phê duyệt từ Nhà tài trợ dự án / Khách hàng giả định.

## 9. Related Documents

- [Master Plan](../08-project/master-plan.md)
- [Master Plan Excel](../08-project/master-plan.xlsx)
- [Work Breakdown Structure](../08-project/wbs.md)
- [Risk Register](../08-project/risk-register.md)
- [RACI Matrix](../08-project/raci-matrix.md)
- [Team Charter](../08-project/team-charter.md)
- [Feedback Process](../10-product-management/feedback-process.md)
- [Product Roadmap](../10-product-management/roadmap.md)
- [Quality Plan](../09-quality/quality-plan.md)
- [Traceability Matrix](../06-acceptance/traceability-matrix.md)
