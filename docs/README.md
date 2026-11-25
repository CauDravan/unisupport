# UniSupport Documentation Guide

## 1. Purpose

Thư mục `docs/` lưu trữ các tài liệu phân tích, thiết kế, lập kế hoạch, kiểm thử và quản lý dự án **UniSupport – Student Support Management System**.

Tài liệu được sắp xếp theo từng nhóm chủ đề và theo luồng tìm hiểu từ tổng quan sản phẩm đến yêu cầu, thiết kế, kiểm thử và quản lý dự án. Thành viên nhóm có thể sử dụng README này làm điểm bắt đầu để tìm đúng tài liệu cần xem.

UniSupport được xây dựng trong phạm vi project prototype cho Aurora University (Simulated Client). Các nội dung cần Sponsor hoặc nhóm xác nhận được giữ ở trạng thái `TBD`/cần xác nhận trong tài liệu liên quan; không nên hiểu chúng là quyết định đã được phê duyệt.

## 2. Recommended Reading Order

Để hiểu dự án theo trình tự, nên đọc tài liệu theo thứ tự sau:

| Order | Documentation | What to understand |
|---|---|---|
| 1 | [Product Overview](./01-product/README.md) | Bối cảnh, vấn đề cần giải quyết, các Actor, mục tiêu và giới hạn của UniSupport. |
| 2 | [Domain Overview](./02-domain/domain-overview.md) | Các khái niệm nghiệp vụ chính và cách các đối tượng trong hệ thống liên hệ với nhau. |
| 3 | [Modules](./03-modules/README.md) | Cách chia hệ thống thành 4 Modules, người dùng chính và quan hệ phụ thuộc giữa các Modules. |
| 4 | [Workflows](./04-workflows/) | Trình tự nghiệp vụ từ khi Student gửi Request đến khi Staff xử lý, đóng Request và Student gửi Feedback. |
| 5 | [Requirements](./05-requirements/README.md) | Các chức năng hệ thống phải cung cấp và các tiêu chí chất lượng cần đáp ứng. |
| 6 | [Acceptance & Testing](./06-acceptance/) | Điều kiện nghiệm thu, Test Scenarios và mối liên kết giữa yêu cầu, kiểm thử, công việc, Milestone và Quotation. |
| 7 | [Architecture](./07-architecture/) | Ranh giới hệ thống, kiến trúc logic, mô hình dữ liệu và các yêu cầu dữ liệu. |
| 8 | [Project Management](./08-project/) | Project Proposal, phạm vi, kế hoạch, WBS, nguồn lực, trách nhiệm, rủi ro và báo giá. |
| 9 | [Quality Management](./09-quality/quality-plan.md) | Cách nhóm thực hiện Quality Assurance, Quality Control, kiểm thử và quản lý lỗi. |
| 10 | [Product Management](./10-product-management/) | Cách tiếp nhận Feedback, theo dõi Success Metrics và định hướng Feature Roadmap. |
| 11 | [Project Governance](./11-governance/project-governance.md) | Cách theo dõi dự án, báo cáo, xử lý vấn đề và kiểm soát thay đổi. |

Nếu chỉ cần tra cứu một nội dung cụ thể, có thể sử dụng bảng Document Directory ở mục 3 thay vì đọc toàn bộ tài liệu theo thứ tự.

## 3. Document Directory

### 3.1 Product Overview — `docs/01-product/`

| File | Nội dung |
|---|---|
| [README.md](./01-product/README.md) | Tổng quan sản phẩm, Problem, Actors, Goals và Non-goals. |
| [problem-statement.md](./01-product/problem-statement.md) | Mô tả vấn đề hiện tại trong việc tiếp nhận và quản lý yêu cầu hỗ trợ sinh viên. |
| [product-goals.md](./01-product/product-goals.md) | Các mục tiêu mà UniSupport hướng đến. |
| [product-scope.md](./01-product/product-scope.md) | Phạm vi chức năng thuộc dự án và các nội dung chưa nằm trong phạm vi hiện tại. |
| [product-backlog.md](./01-product/product-backlog.md) | Danh sách các hạng mục sản phẩm cần xem xét và phát triển. |

### 3.2 Domain — `docs/02-domain/`

| File | Nội dung |
|---|---|
| [domain-overview.md](./02-domain/domain-overview.md) | Tổng quan miền nghiệp vụ và các khái niệm chính của UniSupport. |
| [request-model.md](./02-domain/request-model.md) | Mô tả Request và các thông tin nghiệp vụ liên quan. |
| [request-status.md](./02-domain/request-status.md) | Định nghĩa các Request Status và ý nghĩa của từng trạng thái. |
| [users-and-roles.md](./02-domain/users-and-roles.md) | Các nhóm User, Role và trách nhiệm tương ứng. |
| [business-rules.md](./02-domain/business-rules.md) | Các quy tắc nghiệp vụ chi phối việc tạo, phân công, xử lý và đóng Request. |

### 3.3 Modules — `docs/03-modules/`

Bắt đầu từ [Module Overview](./03-modules/README.md), sau đó mở README và PRD của Module cần tìm hiểu.

| Module | Documentation | Nội dung chính |
|---|---|---|
| M01 — Student Portal | [README](./03-modules/M01-student-portal/README.md) · [PRD](./03-modules/M01-student-portal/prd.md) | Chức năng dành cho Student, tập trung vào Student Request Submission, Request Tracking và Feedback. |
| M02 — Staff Workspace | [README](./03-modules/M02-staff-workspace/README.md) · [PRD](./03-modules/M02-staff-workspace/prd.md) | Chức năng hỗ trợ Staff tiếp nhận, phân loại, phân công và xử lý Request. |
| M03 — Management Dashboard | [README](./03-modules/M03-management-dashboard/README.md) · [PRD](./03-modules/M03-management-dashboard/prd.md) | Chức năng theo dõi tình hình Request và cung cấp thông tin tổng hợp cho Management. |
| M04 — Security and Access | [README](./03-modules/M04-security-and-access/README.md) · [PRD](./03-modules/M04-security-and-access/prd.md) | Các yêu cầu liên quan đến xác thực, Role, quyền truy cập và bảo vệ dữ liệu. |

### 3.4 Workflows — `docs/04-workflows/`

Các tài liệu dưới đây mô tả quy trình nghiệp vụ theo từng bước. Có thể đọc theo thứ tự WF-01 đến WF-07:

| Workflow | File | Nội dung |
|---|---|---|
| WF-01 — Submit Request | [WF-01-submit-request.md](./04-workflows/WF-01-submit-request.md) | Student gửi Support Request. |
| WF-02 — Classify and Assign | [WF-02-classify-and-assign.md](./04-workflows/WF-02-classify-and-assign.md) | Staff phân loại Request và xác định Department/Assigned Staff. |
| WF-03 — Process Request | [WF-03-process-request.md](./04-workflows/WF-03-process-request.md) | Staff thực hiện xử lý và cập nhật tiến độ Request. |
| WF-04 — Request Additional Information | [WF-04-request-additional-information.md](./04-workflows/WF-04-request-additional-information.md) | Staff yêu cầu Student cung cấp thông tin bổ sung. |
| WF-05 — Transfer Request | [WF-05-transfer-request.md](./04-workflows/WF-05-transfer-request.md) | Staff chuyển Request cho Staff hoặc Department phù hợp. |
| WF-06 — Resolve and Close | [WF-06-resolve-and-close.md](./04-workflows/WF-06-resolve-and-close.md) | Staff ghi nhận kết quả xử lý và đóng Request theo điều kiện nghiệp vụ. |
| WF-07 — Feedback | [WF-07-feedback.md](./04-workflows/WF-07-feedback.md) | Student gửi Feedback sau khi Request được xử lý. |

### 3.5 Requirements — `docs/05-requirements/`

Bắt đầu từ [Requirements README](./05-requirements/README.md).

| File | Nội dung |
|---|---|
| [functional-requirements.md](./05-requirements/functional-requirements.md) | Functional Requirements (FR), Actor, Priority, Preconditions, Main Flow, Business Rules, Alternative/Error Flows, Acceptance Criteria và Edge Cases. |
| [non-functional-requirements.md](./05-requirements/non-functional-requirements.md) | Non-Functional Requirements (NFR), các tiêu chí Performance, Usability, Security/Access Control, Reliability và phương pháp đánh giá. |

### 3.6 Acceptance & Testing — `docs/06-acceptance/`

| File | Nội dung |
|---|---|
| [acceptance-criteria.md](./06-acceptance/acceptance-criteria.md) | Các Acceptance Criteria tổng quát dùng để đánh giá kết quả của hệ thống. |
| [test-scenarios.md](./06-acceptance/test-scenarios.md) | Các Test Scenarios dùng để kiểm tra Functional Requirements, Non-Functional Requirements và các luồng nghiệp vụ liên quan. |
| [traceability-matrix.md](./06-acceptance/traceability-matrix.md) | Theo dõi liên kết giữa Requirements, Acceptance Criteria, Test Scenarios, WBS Parent Tasks, Milestones và Quotation. |

**Lưu ý khi đối chiếu mã:** `acceptance-criteria.md` sử dụng mã Generic AC; các Acceptance Criteria nằm bên trong từng FR trong `functional-requirements.md` là mã chi tiết theo Requirement. Cần xem đúng ngữ cảnh và Traceability Matrix để tránh nhầm hai nhóm mã này. Test Scenario chỉ mô tả cách kiểm thử; không được xem là kết quả Pass nếu chưa thực sự thực thi và ghi nhận kết quả.

### 3.7 Architecture — `docs/07-architecture/`

Nên đọc theo thứ tự System Context → Architecture Overview → ERD → Data Requirements:

| File | Nội dung |
|---|---|
| [system-context.md](./07-architecture/system-context.md) | Xác định System Boundary, Actors, các tương tác chính và những nội dung nằm ngoài phạm vi hiện tại. |
| [architecture-overview.md](./07-architecture/architecture-overview.md) | Trình bày kiến trúc logic và trách nhiệm chính của các thành phần trong hệ thống. |
| [erd.md](./07-architecture/erd.md) | Mô tả các thực thể dữ liệu và quan hệ giữa chúng ở mức Conceptual/Logical. |
| [data-requirements.md](./07-architecture/data-requirements.md) | Mô tả các yêu cầu đối với dữ liệu, thuộc tính và quy tắc dữ liệu liên quan. |

Các tài liệu Architecture mô tả thiết kế ở mức logic phục vụ prototype; không tự xác định công nghệ, database, hosting hoặc production integration khi các quyết định này chưa được chốt.

### 3.8 Project Management — `docs/08-project/`

| File | Nội dung |
|---|---|
| [project-proposal.md](./08-project/project-proposal.md) | Source Markdown của Project Proposal. Bản Word làm việc: [project-proposal.docx](./08-project/project-proposal.docx); PDF review: [project-proposal.pdf](./08-project/project-proposal.pdf). Các bản này chưa được ghi nhận là đã gửi client. |
| [master-plan.md](./08-project/master-plan.md) | Giải thích cấu trúc và nguyên tắc quản lý Master Plan. |
| [master-plan.xlsx](./08-project/master-plan.xlsx) | Nguồn dữ liệu chính thức cho Milestones, WBS, Resources, Gantt và Change Log theo Master Plan. |
| [wbs.md](./08-project/wbs.md) | Giải thích cấu trúc và nguyên tắc quản lý WBS; bảng WBS, effort, dates và dependencies chỉ nằm trong Master Plan Excel. |
| [quotation.xlsx](./08-project/quotation.xlsx) | Bảng Quotation, các hạng mục chi phí, effort, rates và cách tính tổng theo dữ liệu trong bảng. |
| [raci-matrix.md](./08-project/raci-matrix.md) | Phân định Responsible, Accountable, Consulted và Informed cho các công việc/deliverables. |
| [team-charter.md](./08-project/team-charter.md) | Nguyên tắc làm việc, vai trò thành viên, ra quyết định, phối hợp và xử lý vấn đề trong nhóm. |
| [risk-register.md](./08-project/risk-register.md) | Danh sách rủi ro, đánh giá và phương án ứng phó. |
| [assumptions.md](./08-project/assumptions.md) | Các giả định đang được sử dụng khi lập kế hoạch và phân tích dự án. |
| [constraints.md](./08-project/constraints.md) | Các giới hạn ảnh hưởng đến phạm vi và cách thực hiện dự án. |
| [open-questions.md](./08-project/open-questions.md) | Những vấn đề còn cần nhóm hoặc Sponsor xác nhận trước khi chốt quyết định. |
| [team-charter.md — Definition of Done](./08-project/team-charter.md#10-quality-standards--definition-of-done) | Quality Standards & Definition of Done, các điều kiện để một task được xem là hoàn thành. |

**Lưu ý về Project Baseline:** `master-plan.xlsx` là nguồn tham chiếu chính cho lịch trình chi tiết. Khi kiểm tra Milestone hoặc tiến độ trên GitHub, cần đối chiếu mã `MS-xx` và ngày tương ứng với Master Plan. Ngày bắt đầu được ghi là tentative trong `master-plan.md` cho đến khi nhóm xác nhận Project Baseline.

### 3.9 Quality Management — `docs/09-quality/`

| File | Nội dung |
|---|---|
| [quality-plan.md](./09-quality/quality-plan.md) | Mô tả Quality Objectives, Quality Assurance, Quality Control/Testing, Quality Criteria, Defect Management, Deliverable Acceptance, trách nhiệm và Quality Records. |

### 3.10 Product Management — `docs/10-product-management/`

| File | Nội dung |
|---|---|
| [feedback-process.md](./10-product-management/feedback-process.md) | Quy trình tiếp nhận, phân loại, đánh giá và xử lý Feedback về sản phẩm. |
| [success-metrics.md](./10-product-management/success-metrics.md) | Các chỉ số dùng để theo dõi kết quả và mức độ đạt mục tiêu sản phẩm. |
| [roadmap.md](./10-product-management/roadmap.md) | Định hướng các tính năng và cải tiến sản phẩm theo thứ tự ưu tiên. |

### 3.11 Project Governance — `docs/11-governance/`

| File | Nội dung |
|---|---|
| [project-governance.md](./11-governance/project-governance.md) | Quy định theo dõi tiến độ, báo cáo, escalation, quản lý thay đổi và trách nhiệm phê duyệt trong dự án. |

Ngoài tài liệu tham chiếu trong `docs/`, repository còn có GitHub templates tại:

- `.github/ISSUE_TEMPLATE/1-parent-task.md`
- `.github/ISSUE_TEMPLATE/2-bug.md`
- `.github/ISSUE_TEMPLATE/3-feedback.md`
- `.github/ISSUE_TEMPLATE/4-change-request.md`
- `.github/pull_request_template.md`

Các templates này hỗ trợ nhóm tạo Parent Task, ghi nhận Bug, Feedback, Change Request và Pull Request theo cấu trúc thống nhất.

## 4. Cross-Document Reference Guide

Khi cần kiểm tra tính nhất quán giữa các tài liệu, sử dụng luồng tham chiếu sau:

| Nội dung cần kiểm tra | Tài liệu cần đối chiếu |
|---|---|
| Product scope và chức năng được cam kết | Product Scope → Module PRDs → Functional Requirements |
| Quy trình nghiệp vụ và trạng thái Request | Domain Rules/Request Status → Workflows → Functional Requirements |
| Điều kiện nghiệm thu và kiểm thử | Functional/Non-Functional Requirements → Acceptance Criteria → Test Scenarios → Traceability Matrix |
| Thiết kế hệ thống và dữ liệu | System Context → Architecture Overview → ERD → Data Requirements |
| Kế hoạch, effort và thời hạn | Master Plan Excel → WBS → GitHub Milestones/Issues |
| Chi phí và effort được báo giá | Quotation Excel ↔ WBS/Master Plan ↔ Project Proposal |
| Chất lượng và điều kiện bàn giao | Quality Plan → Acceptance Criteria → Test Scenarios/Defect Records |
| Thay đổi sản phẩm và dự án | Feedback Process/Product Backlog → Change Control/Master Plan Change Log → GitHub Change Request |

Khi có nội dung không thống nhất, cần xác định tài liệu nguồn có thẩm quyền cho nội dung đó, ghi nhận vấn đề và cập nhật các tài liệu liên quan. Không tự suy diễn để biến một nội dung `TBD` thành quyết định đã được phê duyệt.

## 5. Document Maintenance

- Mỗi tài liệu cần sử dụng đúng tên gọi và ID đã thống nhất, ví dụ `M01–M04`, `WF-01–WF-07`, `FR-xx`, `NFR-xx`, `TS-xxx` và `MS-xx`.
- Khi thay đổi Requirement, Workflow, Acceptance Criteria, Test Scenario, WBS hoặc Milestone, cần kiểm tra và cập nhật các tài liệu có liên quan, đặc biệt là Traceability Matrix.
- Thay đổi ảnh hưởng đến Scope, Schedule, Effort, Resources hoặc Deliverables cần tuân theo Change Control được mô tả trong Master Plan và Project Governance.
- Các quyết định chưa được nhóm hoặc Sponsor xác nhận phải được ghi rõ là `TBD`, `Tentative` hoặc `Pending Confirmation` tùy ngữ cảnh.
- `master-plan.xlsx` được sử dụng làm nguồn dữ liệu chính cho lịch trình và các thông tin quản lý kế hoạch được nêu trong Master Plan.

---

**Start here:** Nếu đây là lần đầu tìm hiểu UniSupport, hãy bắt đầu từ [Product Overview](./01-product/README.md), sau đó đọc lần lượt theo mục [Recommended Reading Order](#2-recommended-reading-order).


### Bug reporting template

- [Bug Report template](../.github/ISSUE_TEMPLATE/2-bug.md) — dùng Severity Critical/High/Medium/Low theo Quality Plan, kèm owner, target date và verification evidence.
