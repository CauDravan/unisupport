# Work Breakdown Structure (WBS)

## 1. Purpose

Work Breakdown Structure (WBS) được sử dụng để phân chia toàn bộ công việc của dự án UniSupport thành các work packages nhỏ hơn, giúp nhóm xác định những công việc cần thực hiện, trách nhiệm chính và kết quả cần bàn giao.

WBS là cơ sở để:

- Xác định và tổ chức các hoạt động cần thiết để hoàn thành dự án.
- Hỗ trợ ước lượng effort cho từng work package.
- Xác định dependencies giữa các công việc.
- Phối hợp phân công trách nhiệm theo RACI Matrix và Resources.
- Tạo và quản lý các công việc chi tiết thông qua GitHub Issues.
- Theo dõi tiến độ và effort trong suốt vòng đời dự án.

WBS được xây dựng dựa trên Project Proposal và Master Plan Excel, với tổng thời gian thực hiện 15 tuần và giới hạn tối đa 320 person-hours.

File `master-plan.xlsx` là nguồn dữ liệu chính thức cho WBS IDs, work packages, effort estimates, schedule, dependencies và resource allocation. Tài liệu này giải thích cấu trúc và nội dung công việc ở mức tổng quan.

## 2. WBS Structure

WBS của dự án được tổ chức thành 9 nhóm công việc chính, sử dụng mã WBS thống nhất với sheet WBS trong `master-plan.xlsx`.

Các nhóm công việc bao gồm:

1. Project Initiation & Analysis.
2. Requirements & Solution Design.
3. MS-01 – Student Request Submission & Tracking.
4. MS-02 – Staff Request Classification & Processing.
5. MS-03 – Request Transfer, Resolution & Feedback.
6. MS-04 – Management Dashboard, Security & Handover.
7. Project Management & Control.
8. Documentation & Handover.
9. Contingency Reserve.

Các nhóm 3–6 được tổ chức theo incremental development, nghĩa là nhóm hoàn thiện và bàn giao từng phần chức năng theo milestone thay vì chờ toàn bộ prototype hoàn thành mới tiến hành kiểm thử.

### 2.1 Project Initiation & Analysis

**Duration:** Week 1–2

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 1.1 | Project Kick-off & Planning | Thống nhất mục tiêu dự án, cách làm việc và phương thức giao tiếp. Kết quả: Kick-off notes và initial project plan. | PM | 5h |
| 1.2 | Stakeholder & Problem Analysis | Xác định stakeholder và phân tích các vấn đề trong quy trình hỗ trợ sinh viên. Kết quả: Problem analysis và stakeholder information. | BA | 6h |
| 1.3 | Scope & Requirements Baseline | Xác định và thống nhất phạm vi dự án ban đầu dựa trên Project Proposal. Kết quả: Product Scope documentation. | BA | 6h |
| 1.4 | Project Workspace & Risk Setup | Thiết lập repository, GitHub và ghi nhận các rủi ro ban đầu. Kết quả: Project workspace và initial Risk Register. | PM | 5h |

**Group Deliverables:**
- Project kick-off notes and initial project plan.
- Stakeholder and problem analysis.
- Initial Product Scope.
- Shared project workspace.
- Initial Risk Register.

### 2.2 Requirements & Solution Design

**Duration:** Week 3–6

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 2.1 | Business Workflow & Rules Design | Xây dựng workflow WF-01 đến WF-07 và các business rules cho quá trình tiếp nhận, phân loại, phân công và xử lý yêu cầu. Kết quả: Business workflows and rules documentation. | BA | 14h |
| 2.2 | Functional & Non-functional Requirements | Xác định FR, NFR và Acceptance Criteria cho hệ thống. Kết quả: Requirements documentation and acceptance criteria. | BA | 12h |
| 2.3 | System Architecture, API & ERD | Xác định kiến trúc prototype, API outline, cấu trúc dữ liệu và quan hệ giữa các entities. Kết quả: Architecture overview, API outline and ERD. | BE | 10h |
| 2.4 | UX/UI Design | Thiết kế user flows và wireframes cho Student, Staff và Management. Kết quả: User flows and wireframes. | FE | 14h |
| 2.5 | Solution Design Review | Rà soát tính nhất quán giữa requirements, workflows và technical design. Kết quả: Design review notes and updated design documents. | PM | 5h |

**Group Deliverables:**
- Business workflows WF-01 to WF-07.
- Business rules documentation.
- Functional and non-functional requirements.
- Acceptance Criteria.
- System architecture and API outline.
- Entity Relationship Diagram (ERD).
- User flows and wireframes.
- Design review results.

### 2.3 MS-01 – Student Request Submission & Tracking

**Duration:** Week 6–9

**Milestone:** MS-01 – Student Request Submission & Tracking

**Milestone Completion:** Week 9 – 15/01/2027

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 3.1 | Development Environment & Simulated Data | Chuẩn bị môi trường phát triển, cấu trúc database và dữ liệu giả lập. Kết quả: Development environment and simulated dataset. | BE | 6h |
| 3.2 | Authentication & Access Control | Xây dựng cơ chế đăng nhập và phân quyền cơ bản theo role. Kết quả: Authentication and role-based access control. | BE | 7h |
| 3.3 | Student Request API | Xây dựng API hỗ trợ gửi yêu cầu và theo dõi yêu cầu. Kết quả: Student request APIs. | BE | 6h |
| 3.4 | Student Portal Development | Xây dựng giao diện gửi yêu cầu, xem danh sách, trạng thái và lịch sử cập nhật. Kết quả: Student Portal prototype. | FE | 14h |
| 3.5 | MS-01 Test Scenario Preparation | Chuẩn bị các tình huống kiểm thử và Acceptance Criteria cho MS-01. Kết quả: MS-01 test scenarios and test cases. | BA | 4h |
| 3.6 | MS-01 Testing | Kiểm thử chức năng gửi và theo dõi yêu cầu, bao gồm regression testing khi cần thiết. Kết quả: MS-01 test results. | BA | 4h |
| 3.7 | MS-01 Defect Resolution | Ghi nhận và sửa các lỗi được phát hiện trong quá trình kiểm thử MS-01. Kết quả: Updated MS-01 prototype and defect records. | BE | 3h |
| 3.8 | MS-01 Handover & Client Feedback | Chuẩn bị và bàn giao chức năng MS-01, tiếp nhận feedback từ client. Kết quả: MS-01 handover and feedback records. | PM | 3h |

**Related Workflow / Requirements:**
- WF-01.
- FR-STU-01.
- FR-STU-02.
- FR-SEC-01.
- NFR-SEC-07.

**Group Deliverables:**
- Development environment and simulated dataset.
- Authentication and access control.
- Student request APIs.
- Student Portal prototype.
- MS-01 test scenarios and results.
- Updated prototype after defect resolution.
- MS-01 handover and client feedback.

### 2.4 MS-02 – Staff Request Classification & Processing

**Duration:** Week 9–11

**Milestone:** MS-02 – Staff Request Classification & Processing

**Milestone Completion:** Week 11 – 29/01/2027

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 4.1 | Classification & Assignment API | Xây dựng API phân loại, phân công và quản lý hàng đợi yêu cầu. Kết quả: Classification, assignment and queue APIs. | BE | 6h |
| 4.2 | Request Processing API & Activity Log | Xây dựng API xử lý yêu cầu, yêu cầu bổ sung thông tin và ghi nhận Activity Log. Kết quả: Request processing APIs and activity records. | BE | 7h |
| 4.3 | Staff Workspace Development | Xây dựng giao diện hàng đợi, phân loại, phân công và xử lý yêu cầu cho Staff. Kết quả: Staff Workspace prototype. | FE | 15h |
| 4.4 | Student Notification & Additional Information | Xây dựng chức năng thông báo và gửi thông tin bổ sung cho Student. Kết quả: Student notification and additional information functionality. | FE | 6h |
| 4.5 | MS-02 Test Scenario Preparation | Chuẩn bị tình huống kiểm thử và Acceptance Criteria cho MS-02. Kết quả: MS-02 test scenarios and test cases. | BA | 3h |
| 4.6 | MS-02 Testing & MS-01 Regression | Kiểm thử phân loại, phân công, xử lý yêu cầu và regression testing cho MS-01. Kết quả: MS-02 test and regression results. | BA | 5h |
| 4.7 | MS-02 Defect Resolution | Ghi nhận và sửa lỗi được phát hiện trong quá trình kiểm thử MS-02. Kết quả: Updated MS-02 prototype and defect records. | BE | 3h |
| 4.8 | MS-02 Handover & Client Feedback | Bàn giao chức năng MS-02 và tiếp nhận feedback từ client. Kết quả: MS-02 handover and feedback records. | PM | 3h |

**Related Workflow / Requirements:**
- WF-02, WF-03, WF-04.
- FR-STA-01.
- FR-STA-02.
- FR-STA-03.
- FR-STU-02.
- FR-STU-03.

**Group Deliverables:**
- Classification and assignment APIs.
- Request processing APIs and Activity Log.
- Staff Workspace prototype.
- Student notification and additional information functionality.
- MS-02 test scenarios and results.
- MS-01 regression test results.
- Updated prototype after defect resolution.
- MS-02 handover and client feedback.

### 2.5 MS-03 – Request Transfer, Resolution & Feedback

**Duration:** Week 11–13

**Milestone:** MS-03 – Request Transfer, Resolution & Feedback

**Milestone Completion:** Week 13 – 12/02/2027

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 5.1 | Request Transfer & Resolution API | Xây dựng API chuyển giao, giải quyết và đóng yêu cầu. Kết quả: Request transfer and resolution APIs. | BE | 7h |
| 5.2 | Student Feedback API | Xây dựng API tiếp nhận feedback của sinh viên sau khi yêu cầu được giải quyết. Kết quả: Student feedback API. | BE | 3h |
| 5.3 | Staff Transfer & Resolution Interface | Xây dựng giao diện cho Staff chuyển giao, giải quyết và đóng yêu cầu. Kết quả: Staff transfer and resolution interface. | FE | 6h |
| 5.4 | Student Resolution & Feedback Interface | Xây dựng giao diện giúp Student xem kết quả xử lý và gửi feedback. Kết quả: Student resolution and feedback interface. | FE | 4h |
| 5.5 | MS-03 Test Scenario Preparation | Chuẩn bị tình huống kiểm thử và Acceptance Criteria cho MS-03. Kết quả: MS-03 test scenarios and test cases. | BA | 3h |
| 5.6 | MS-03 Testing & Regression | Kiểm thử chuyển giao, giải quyết, đóng yêu cầu và regression testing cho MS-01, MS-02. Kết quả: MS-03 test and regression results. | BA | 4h |
| 5.7 | MS-03 Defect Resolution | Ghi nhận và sửa lỗi được phát hiện trong quá trình kiểm thử MS-03. Kết quả: Updated MS-03 prototype and defect records. | BE | 3h |
| 5.8 | MS-03 Handover & Client Feedback | Bàn giao chức năng MS-03 và tiếp nhận feedback từ client. Kết quả: MS-03 handover and feedback records. | PM | 3h |

**Related Workflow / Requirements:**
- WF-05, WF-06, WF-07.
- FR-STA-03.
- FR-STU-03.

**Group Deliverables:**
- Request transfer and resolution APIs.
- Student feedback API.
- Staff transfer and resolution interface.
- Student resolution and feedback interface.
- MS-03 test scenarios and results.
- MS-01 and MS-02 regression test results.
- Updated prototype after defect resolution.
- MS-03 handover and client feedback.

### 2.6 MS-04 – Management Dashboard, Security & Handover

**Duration:** Week 11–15

**Milestone:** MS-04 – Management Dashboard, Security & Handover

**Milestone Completion:** Week 15 – 26/02/2027

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 6.1 | Management Dashboard API & Reporting | Xây dựng API cung cấp dữ liệu dashboard và báo cáo quản lý. Kết quả: Management dashboard and reporting APIs. | BE | 7h |
| 6.2 | System-wide Security & Audit Log Review | Rà soát phân quyền và Activity/Audit Log trên toàn hệ thống. Kết quả: Security and audit log review results. | BE | 5h |
| 6.3 | Management Dashboard Development | Xây dựng giao diện dashboard giúp Management theo dõi các chỉ số và báo cáo chính. Kết quả: Management Dashboard prototype. | FE | 10h |
| 6.4 | Responsive, Bilingual & Usability Evaluation | Hoàn thiện giao diện responsive, hỗ trợ tiếng Việt và tiếng Anh, đồng thời đánh giá usability. Kết quả: Responsive and bilingual interface with usability evaluation results. | FE | 6h |
| 6.5 | MS-04 Test Scenario Preparation | Chuẩn bị tình huống kiểm thử và Acceptance Criteria cho MS-04. Kết quả: MS-04 test scenarios and test cases. | BA | 3h |
| 6.6 | Full System Testing & Final Acceptance | Kiểm thử toàn hệ thống, thực hiện regression testing cho MS-01 đến MS-04 và chuẩn bị nghiệm thu. Kết quả: Full system test and acceptance results. | BA | 6h |
| 6.7 | MS-04 Backend Defect Resolution | Sửa các lỗi backend được phát hiện trong quá trình kiểm thử cuối. Kết quả: Updated backend components and defect records. | BE | 3h |
| 6.8 | MS-04 UI Defect Resolution & Final Regression | Sửa lỗi giao diện và thực hiện final regression testing. Kết quả: Updated interface and final regression results. | FE | 4h |
| 6.9 | MS-04 Handover & Client Feedback | Hoàn tất bàn giao MS-04 và tiếp nhận feedback cuối cùng từ client. Kết quả: Final milestone handover and feedback records. | PM | 3h |

**Related Workflow / Requirements:**
- FR-MGT-01.
- FR-MGT-02.
- FR-SEC-01.
- FR-SEC-02.
- NFR-COMP-01.
- NFR-COMP-02.
- NFR-USE-*.

**Group Deliverables:**
- Management dashboard and reporting APIs.
- Security and audit log review results.
- Management Dashboard prototype.
- Responsive and bilingual interface.
- Usability evaluation results.
- MS-04 test scenarios and results.
- Full system regression and acceptance results.
- Updated prototype after defect resolution.
- Final milestone handover and client feedback.

### 2.7 Project Management & Control

**Duration:** Week 1–15

Nhóm công việc này được thực hiện xuyên suốt dự án nhằm theo dõi tiến độ, kiểm soát effort, quản lý rủi ro và xử lý các thay đổi trong kế hoạch.

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 7.1 | Project Progress Monitoring & Reporting | Theo dõi tiến độ thực tế so với kế hoạch, tổng hợp tình trạng công việc và báo cáo các sai lệch. Kết quả: Project progress reports. | PM | 15h |
| 7.2 | Risk Management & Change Control | Theo dõi Risk Register, đánh giá ảnh hưởng của change requests và cập nhật Change Log sau khi thay đổi được chấp thuận. Kết quả: Updated Risk Register and Change Log. | PM | 12h |

**Group Deliverables:**
- Project progress reports.
- Planned versus actual effort tracking.
- Updated Risk Register.
- Change request assessment records.
- Updated Change Log.

### 2.8 Documentation & Handover

**Duration:** Week 14–15

Nhóm công việc này tập trung hoàn thiện tài liệu và chuẩn bị gói bàn giao để client hoặc một nhóm khác có thể tiếp nhận prototype và tiếp tục sử dụng tài liệu dự án.

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 8.1 | Technical Documentation & Installation Guide | Chuẩn bị tài liệu kỹ thuật, cấu hình và hướng dẫn cài đặt hệ thống. Kết quả: Technical documentation and installation guide. | BE | 3h |
| 8.2 | Project Documentation & User Guide | Hoàn thiện tài liệu dự án và hướng dẫn sử dụng các chức năng chính cho Student, Staff và Management. Kết quả: Project documentation and user guide. | BA | 8h |
| 8.3 | Project Handover Package Preparation | Tập hợp source code, tài liệu, dữ liệu giả lập và các thành phần cần thiết cho việc bàn giao. Kết quả: Project handover package. | PM | 8h |
| 8.4 | Final Handover Review | Kiểm tra tính đầy đủ, nhất quán và khả năng tiếp nhận của gói bàn giao. Kết quả: Handover review and confirmation records. | PM | 6h |

**Group Deliverables:**
- Technical documentation.
- Installation Guide.
- Project documentation.
- User Guide.
- Project Handover Package.
- Handover review results.

### 2.9 Contingency Reserve

**Duration:** Week 1–15

| WBS ID | Work Package | Description & Expected Deliverable | Lead Role | Effort |
|---|---|---|---|---:|
| 9.1 | Contingency Reserve for Change Requests & Risks | Dự phòng effort để xử lý các change requests hoặc rủi ro phát sinh đã được xem xét và chấp thuận. Kết quả: Approved reserve usage records and updated effort tracking. | Contingency Reserve | 16h |

**Notes:**

- Contingency Reserve được quản lý riêng và không phải effort mặc định để thực hiện các công việc đã có trong WBS.
- Việc sử dụng reserve cần có lý do và được ghi nhận trong Change Log.
- Effort sửa lỗi đã được tính trong các work packages tương ứng, không được tính trùng vào Contingency Reserve.

## 3. Effort Estimation Summary

Tổng effort được ước lượng dựa trên các work packages trong Master Plan Excel. Tổng planned effort không bao gồm contingency reserve là 304 person-hours.

### 3.1 Effort by WBS Group

| WBS Group | Estimated Effort |
|---|---:|
| 1. Project Initiation & Analysis | 22h |
| 2. Requirements & Solution Design | 55h |
| 3. MS-01 Delivery | 47h |
| 4. MS-02 Delivery | 48h |
| 5. MS-03 Delivery | 33h |
| 6. MS-04 Delivery | 47h |
| 7. Project Management & Control | 27h |
| 8. Documentation & Handover | 25h |
| **Total Planned Effort** | **304h** |
| Contingency Reserve | 16h |
| **Maximum Effort Limit** | **320h** |

### 3.2 Effort Allocation Baseline by Team Role

Mức phân bổ effort dự kiến cho từng vai trò được xác định trong sheet Resources của Master Plan Excel.

| Team Role | Planned Effort |
|---|---:|
| Project Manager (PM) | 68h |
| Business Analyst (BA) | 78h |
| Front-end Developer (FE) | 79h |
| Back-end Developer (BE) | 79h |
| **Total Planned Effort** | **304h** |
| Contingency Reserve | 16h |
| **Maximum Effort** | **320h** |

**Effort Allocation Notes:**

- Effort của từng role được tính dựa trên các work packages được phân công trong WBS.
- Lead Role xác định vai trò chịu trách nhiệm chính trong việc điều phối và dẫn dắt work package.
- Các thành viên khác vẫn có thể tham gia hỗ trợ và đóng góp vào cùng một work package.
- Effort của mỗi work package chỉ được tính một lần trong tổng planned effort, tránh cộng trùng khi có nhiều thành viên cùng tham gia.
- Resources được sử dụng để theo dõi effort allocation, workload và mức độ sử dụng nguồn lực của từng role.
- Planned effort và actual effort được so sánh trong suốt quá trình thực hiện dự án để phát hiện các sai lệch.

## 4. Dependencies & Schedule Management

Dependencies xác định mối quan hệ giữa các work packages và công việc cần hoàn thành trước khi một công việc khác có thể bắt đầu.

Các dependencies chi tiết được quản lý trong cột Dependencies của sheet WBS trong `master-plan.xlsx`.

Nhóm áp dụng các nguyên tắc sau:

- Các work packages có dependency phải được xem xét theo thứ tự thực hiện.
- Các hoạt động phát triển được triển khai theo từng milestone.
- Test Scenario Preparation được thực hiện trước các hoạt động kiểm thử tương ứng.
- Testing và regression testing được thực hiện sau khi các chức năng liên quan đã sẵn sàng.
- Defect Resolution được thực hiện dựa trên kết quả kiểm thử.
- Handover được tiến hành sau khi các điều kiện nghiệm thu tương ứng được đáp ứng.

Các milestone chính của dự án:

| Milestone | Deliverable | Planned Completion |
|---|---|---|
| MS-01 | Student Request Submission & Tracking | 15/01/2027 |
| MS-02 | Staff Request Classification & Processing | 29/01/2027 |
| MS-03 | Request Transfer, Resolution & Feedback | 12/02/2027 |
| MS-04 | Management Dashboard, Security & Handover | 26/02/2027 |

Mỗi milestone có deliverables và acceptance criteria riêng. Việc hoàn thành milestone phải dựa trên kết quả kiểm thử và điều kiện nghiệm thu, không chỉ dựa trên ngày kết thúc công việc.

## 5. WBS Management

WBS được sử dụng cùng với các tài liệu và công cụ quản lý dự án khác:

- **Master Plan Excel:** Nguồn dữ liệu chính thức để quản lý WBS IDs, work packages, effort, schedule, dependencies, resources, milestones và Change Log.
- **Project Schedule:** Tham chiếu lịch trình chính thức trong Master Plan Excel, không duy trì một lịch độc lập có thể gây mâu thuẫn.
- **RACI Matrix:** Xác định trách nhiệm và mức độ tham gia của từng thành viên đối với các hoạt động trong dự án.
- **Resources:** Theo dõi effort allocation, workload và actual effort theo từng vai trò.
- **Risk Register:** Ghi nhận và theo dõi các rủi ro có thể ảnh hưởng đến work packages, effort và tiến độ.
- **GitHub Milestones:** Nhóm các GitHub Issues theo các milestone MS-01 đến MS-04, sử dụng cùng mã và deadline với Master Plan Excel.
- **GitHub Issues:** Theo dõi các task chi tiết, người phụ trách, deadline, trạng thái và actual effort nếu nhóm sử dụng trường theo dõi này.

WBS tập trung vào việc phân rã công việc ở cấp độ lập kế hoạch, không thay thế việc quản lý các task chi tiết trên GitHub.

Khi có thay đổi về project scope, requirements, schedule hoặc resources:

1. Ghi nhận yêu cầu thay đổi.
2. Đánh giá ảnh hưởng đến work packages, dependencies, effort và milestones.
3. Xác định người có trách nhiệm xem xét và phê duyệt.
4. Cập nhật Master Plan Excel sau khi thay đổi được chấp thuận.
5. Đồng bộ các nội dung liên quan trong WBS Markdown, GitHub Issues và các tài liệu dự án khác.
6. Ghi nhận lịch sử thay đổi trong Change Log.

Các WBS IDs phải được giữ thống nhất giữa WBS Markdown, Master Plan Excel và GitHub Issues để bảo đảm khả năng theo dõi và đối chiếu công việc.

---

**Document Location:** `docs/01-project-management/wbs.md`

**Related Documents:**
- `master-plan.xlsx`
- `master-plan.md`
- `team-charter.md`
- `raci-matrix.md`
- `risk-register.md`
- `project-schedule.md` (nếu còn sử dụng, chỉ tham chiếu lịch chính thức)
- `../02-product-management/product-scope.md`
- Product Requirements Document (PRD)
- Project Proposal