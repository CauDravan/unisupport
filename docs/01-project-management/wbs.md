# Work Breakdown Structure (WBS)

## 1. Purpose

Work Breakdown Structure (WBS) được sử dụng để phân chia toàn bộ công việc của dự án UniSupport thành các phases và work packages nhỏ hơn, giúp nhóm xác định những công việc cần thực hiện và kết quả cần bàn giao.

WBS là cơ sở để:
- Xác định và tổ chức các hoạt động cần thiết để hoàn thành dự án.
- Hỗ trợ ước lượng effort cho từng work package.
- Phối hợp phân công trách nhiệm theo RACI Matrix.
- Tạo và quản lý các công việc chi tiết thông qua GitHub Issues.
- Theo dõi tiến độ và effort trong suốt vòng đời dự án.

WBS được xây dựng dựa trên Project Proposal với tổng thời gian thực hiện 15 tuần và giới hạn tối đa 320 person-hours.

## 2. WBS Structure

Dự án được chia thành 6 phases chính, tương ứng với Project Proposal.

### 2.1 Phase 1 – Project Initiation & Analysis

**Duration:** Week 1–2

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 1.1 | Project Kick-off & Planning | Xác định mục tiêu dự án, thống nhất cách làm việc và phương thức giao tiếp giữa các thành viên. | Kick-off notes and initial project plan | PM | 6h |
| 1.2 | Stakeholder & Problem Analysis | Xác định các nhóm stakeholder, tìm hiểu vấn đề trong quy trình tiếp nhận và xử lý yêu cầu hỗ trợ sinh viên. | Stakeholder overview and problem analysis | BA | 8h |
| 1.3 | Scope & Requirements Definition | Làm rõ mục tiêu, phạm vi ban đầu, các yêu cầu chính và những nội dung không thuộc phạm vi dự án. | Initial scope and requirements baseline | BA | 8h |
| 1.4 | Project Workspace & Risk Setup | Thiết lập repository, cấu trúc tài liệu, công cụ theo dõi công việc và ghi nhận các rủi ro ban đầu. | Shared project workspace and initial Risk Register | PM | 6h |

**Phase Deliverables:**
- Project scope and initial requirements.
- Stakeholder overview.
- Shared project workspace.
- Initial Risk Register.

### 2.2 Phase 2 – Solution Design & UX/UI

**Duration:** Week 3–6

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 2.1 | Business Workflow & Rules Design | Xây dựng các workflow và business rules cho quá trình tiếp nhận, phân loại, phân công và xử lý yêu cầu. | Business workflows and rules | BA | 18h |
| 2.2 | Functional & Non-functional Requirements | Xác định các functional requirements, non-functional requirements và acceptance criteria cho hệ thống. | Requirements documentation and acceptance criteria | BA | 14h |
| 2.3 | System Architecture & Data Design | Xác định kiến trúc prototype, API, cấu trúc dữ liệu và quan hệ giữa các entities. | Architecture overview, API outline and ERD | BE | 16h |
| 2.4 | UI/UX Design & Prototype | Thiết kế user flows, wireframes và giao diện prototype cho Student, Staff và Management. | User flows, wireframes and UI prototype | FE | 16h |
| 2.5 | Solution Design Review | Rà soát thiết kế, kiểm tra tính nhất quán giữa requirements, workflows và technical design. | Design review notes and updated design documents | PM | 6h |

**Phase Deliverables:**
- Functional and non-functional requirements.
- Business workflows and rules.
- System architecture and ERD.
- UI/UX prototype.
- Design review results.

### 2.3 Phase 3 – Intermediate Review

**Duration:** Week 7

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 3.1 | Review Preparation | Chuẩn bị tài liệu, prototype và nội dung trình bày để báo cáo tiến độ dự án. | Intermediate review materials | PM | 6h |
| 3.2 | Intermediate Project Review | Trình bày kết quả đã thực hiện và tiếp nhận feedback từ stakeholders. | Intermediate review presentation and feedback | PM | 4h |
| 3.3 | Feedback Assessment & Change Review | Đánh giá feedback, xác định ảnh hưởng đến scope, schedule và effort trước khi thống nhất các thay đổi. | Feedback assessment and change log | BA | 6h |

**Phase Deliverables:**
- Intermediate review presentation.
- Stakeholder feedback.
- Change log and review decisions.

### 2.4 Phase 4 – Prototype Development & Data Simulation

**Duration:** Week 8–11

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 4.1 | Development Environment & Simulated Data | Chuẩn bị môi trường phát triển, cấu trúc database và dữ liệu giả lập phục vụ prototype. | Development environment and simulated dataset | BE | 18h |
| 4.2 | Authentication & Access Control | Xây dựng cơ chế đăng nhập và phân quyền cơ bản cho các nhóm người dùng. | Authentication and role-based access control | BE | 16h |
| 4.3 | Student Portal Development | Xây dựng giao diện và chức năng cho sinh viên gửi yêu cầu, xem danh sách và theo dõi trạng thái yêu cầu. | Student Portal prototype | FE | 24h |
| 4.4 | Staff Workspace Development | Xây dựng các chức năng hỗ trợ nhân viên phân loại, phân công, cập nhật trạng thái và xử lý yêu cầu. | Staff Workspace prototype | BE | 26h |
| 4.5 | Management Dashboard Development | Xây dựng dashboard hỗ trợ theo dõi số lượng yêu cầu, trạng thái xử lý và các thông tin báo cáo cơ bản. | Management Dashboard prototype | FE | 12h |
| 4.6 | Prototype Integration | Kết nối các thành phần frontend và backend, kiểm tra các luồng nghiệp vụ chính giữa các nhóm người dùng. | Integrated prototype | FE | 12h |

**Phase Deliverables:**
- Working development environment.
- Simulated database and data.
- Authentication and access control.
- Student Portal prototype.
- Staff Workspace prototype.
- Management Dashboard prototype.
- Integrated prototype.

### 2.5 Phase 5 – Testing, Evaluation & Refinement

**Duration:** Week 12–14

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 5.1 | Test Planning & Test Case Preparation | Xác định các tình huống kiểm thử, chuẩn bị test cases và dữ liệu giả lập. | Test scenarios and test cases | BA | 12h |
| 5.2 | Functional & Integration Testing | Kiểm tra các chức năng chính, API, luồng nghiệp vụ và khả năng kết nối giữa frontend và backend. | Functional and integration test results | BA | 20h |
| 5.3 | Usability & Responsive Evaluation | Đánh giá mức độ dễ sử dụng và khả năng hiển thị trên thiết bị desktop và mobile. | Usability and responsive evaluation results | FE | 8h |
| 5.4 | Defect Resolution & Prototype Refinement | Ghi nhận lỗi, ưu tiên xử lý các lỗi quan trọng và hoàn thiện prototype dựa trên kết quả kiểm thử. | Updated prototype and defect log | BE | 16h |

**Phase Deliverables:**
- Test scenarios and test cases.
- Functional and integration test results.
- Usability evaluation results.
- Defect log.
- Refined prototype.

### 2.6 Phase 6 – Finalization & Handover

**Duration:** Week 15

| WBS ID | Work Package | Description | Expected Deliverable | Lead Role | Estimated Effort |
|---|---|---|---|---|---:|
| 6.1 | Final Project Documentation | Hoàn thiện các tài liệu dự án, requirements, workflows và các thông tin cần thiết cho việc bàn giao. | Final project documentation | BA | 10h |
| 6.2 | Technical & User Documentation | Chuẩn bị hướng dẫn thiết lập hệ thống, thông tin kỹ thuật và hướng dẫn sử dụng các chức năng chính. | Technical and user guides | BE | 4h |
| 6.3 | Final Presentation Preparation | Chuẩn bị nội dung trình bày, kịch bản demo và tổng hợp kết quả thực hiện dự án. | Final presentation and demo materials | PM | 6h |
| 6.4 | Project Handover | Kiểm tra và sắp xếp source code, tài liệu, dữ liệu giả lập và các thành phần cần thiết để nhóm khác có thể tiếp nhận. | Project handover package | PM | 6h |

**Phase Deliverables:**
- Final project documentation.
- Technical and user guides.
- Final presentation.
- Project handover package.

## 3. Effort Estimation Summary

Tổng effort được ước lượng dựa trên các work packages trong WBS và đối chiếu với giới hạn nguồn lực đã xác định trong Project Proposal.

### 3.1 Effort by Project Phase

| Phase | Estimated Effort |
|---|---:|
| Phase 1 – Project Initiation & Analysis | 28h |
| Phase 2 – Solution Design & UX/UI | 70h |
| Phase 3 – Intermediate Review | 16h |
| Phase 4 – Prototype Development & Data Simulation | 108h |
| Phase 5 – Testing, Evaluation & Refinement | 56h |
| Phase 6 – Finalization & Handover | 26h |
| **Total Planned Effort** | **304h** |
| Contingency Reserve | 16h |
| **Maximum Effort Limit** | **320h** |

### 3.2 Effort Allocation Baseline by Team Role

Mức phân bổ nỗ lực dự kiến cho từng vai trò trong dự án được căn cứ dựa trên Project Proposal.

| Team Role | Planned Effort |
|---|---:|
| Project Manager (PM) | 68 hours |
| Business Analyst (BA) | 78 hours |
| Front-end Developer (FE) | 79 hours |
| Back-end Developer (BE) | 79 hours |
| **Total Planned Effort** | **304 hours** |
| Contingency Reserve | 16 hours |
| **Maximum Effort** | **320 hours** |

**Note:** Mức phân bổ nỗ lực theo vai trò dự án thể hiện mức độ đóng góp kế hoạch tổng thể của từng vai trò, chứ không phải được tính bằng cách cộng thuần túy các ước tính nỗ lực của các gói công việc (work packages) được giao cho vai trò đó. Vai trò Chủ trì (Lead Role) trong mỗi gói công việc xác định vai trò chính chịu trách nhiệm điều phối và dẫn dắt công việc. Các thành viên khác trong nhóm cũng có thể tham gia đóng góp vào cùng gói công việc đó.

Nỗ lực thực tế sẽ được theo dõi sát sao trong quá trình thực hiện dự án và được so sánh với nỗ lực dự kiến nhằm kiểm soát mức độ sử dụng nguồn lực, đồng thời sớm phát hiện các sai lệch có thể xảy ra.

## 4. WBS Management

WBS được sử dụng cùng với các tài liệu và công cụ quản lý dự án khác:

- **Project Schedule:** Xác định thời gian thực hiện và các key milestones tương ứng với các phases trong WBS.
- **RACI Matrix:** Xác định vai trò chịu trách nhiệm chính và các vai trò hỗ trợ cho từng hoạt động.
- **Risk Register:** Ghi nhận và theo dõi các rủi ro có thể ảnh hưởng đến work packages, effort và tiến độ.
- **GitHub Milestones:** Nhóm các GitHub Issues theo project phases hoặc milestones.
- **GitHub Issues:** Theo dõi các task chi tiết, người phụ trách, deadline, trạng thái và actual effort nếu nhóm sử dụng trường theo dõi này.

WBS tập trung vào việc phân rã công việc ở cấp độ lập kế hoạch, không thay thế việc quản lý các task chi tiết trên GitHub.

Khi có thay đổi về project scope hoặc yêu cầu, Project Manager phối hợp với các thành viên liên quan để đánh giá ảnh hưởng đến WBS, Project Schedule và effort trước khi cập nhật kế hoạch.

---

**Document Location:** `docs/01-project-management/wbs.md`

**Related Documents:**
- `project-proposal.docx`
- `team-charter.md`
- `project-schedule.md`
- `raci-matrix.md`
- `risk-register.md`
- `../02-product-management/product-scope.md`
- Product Requirements Document (PRD)