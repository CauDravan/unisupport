# UniSupport – GitHub Issue Content Baseline
Version: Draft for GitHub update
Language convention: English section/function names; Vietnamese descriptions and acceptance criteria.
Source of truth:
- `docs/05-requirements/functional-requirements.md`
- `docs/05-requirements/non-functional-requirements.md`
- `docs/06-acceptance/acceptance-criteria.md`
- `docs/06-acceptance/test-scenarios.md`
- `docs/06-acceptance/traceability-matrix.md`
- `docs/08-project/wbs.md`

## Important rules
1. FR-specific AC IDs below are copied from the current Functional Requirements. Do not renumber them.
2. `FR-STA-03` has no `AC-08` in the source. Do not create one.
3. Project-level `AC-01`–`AC-14` in `acceptance-criteria.md` are a separate AC set from FR-specific ACs. Do not mix the two ID systems.
4. NFR thresholds marked `Proposed baseline` are provisional and require confirmation; they are not approved production commitments.
5. Do not mark an issue complete merely because its acceptance criteria or test scenarios have been written. Actual results/evidence are required.
6. For supporting/project-management issues without a direct functional requirement, use `N/A` and explain why rather than inventing an FR.

---

# MS-01 – Student Request Submission & Tracking

## Issue #1 – Repository Setup
**FR / NFR ID:** N/A – Project Management / Development Setup

**Description**
Thiết lập repository và cấu trúc làm việc chung để các thành viên có thể truy cập source code, tài liệu và đóng góp theo một quy trình thống nhất.

**Acceptance Criteria**
- Repository UniSupport được tạo và các thành viên được cấp quyền truy cập phù hợp.
- Cấu trúc thư mục chính cho source code và project documentation được thiết lập.
- README có hướng dẫn cơ bản về mục tiêu repository, cấu trúc thư mục và cách bắt đầu làm việc.
- Quy tắc branch, commit và Pull Request được ghi lại và có thể truy cập từ repository.
- Một thành viên có thể tạo branch và gửi Pull Request theo quy trình đã thống nhất.

**Evidence**
Repository URL, README và contribution guidelines.

## Issue #2 – Confirm Team Roles and Responsibilities
**FR / NFR ID:** N/A – Project Management

**Description**
Xác định vai trò, trách nhiệm và phạm vi công việc của từng thành viên để tránh bỏ sót hoặc trùng lặp nhiệm vụ trong dự án.

**Acceptance Criteria**
- Các vai trò cần thiết trong nhóm được xác định.
- Mỗi thành viên được ghi nhận vai trò và trách nhiệm chính.
- Trách nhiệm được đối chiếu với Team Charter và RACI Matrix.
- Các work packages chính có vai trò chịu trách nhiệm được xác định.
- Team Charter và RACI Matrix được lưu trong repository và thống nhất với Master Plan.

**Evidence**
Team Charter, RACI Matrix và Resources sheet trong Master Plan.

## Issue #3 – Review Project Proposal and Establish Project Baseline
**FR / NFR ID:** N/A – Project Management / Project Baseline

**Description**
Rà soát Project Proposal và thống nhất baseline ban đầu về mục tiêu, phạm vi, kế hoạch, effort, chi phí và rủi ro của UniSupport.

**Acceptance Criteria**
- Project Proposal được rà soát và các nội dung chưa rõ được ghi nhận.
- Project objective, problem statement, scope và expected deliverables nhất quán giữa Proposal và project documents.
- Master Plan xác định các milestone, planned completion dates, effort và nguồn lực.
- Các giả định, ràng buộc và rủi ro chính được ghi nhận trong tài liệu tương ứng.
- Các nội dung baseline được nhóm thống nhất và có thể truy xuất trong repository.

**Evidence**
Project Proposal, Master Plan, Assumptions, Constraints và Risk Register.

## Issue #4 – Product Scope
**FR / NFR ID:** N/A – Supporting Deliverable; scope baseline for all FRs

**Description**
Xác định rõ chức năng nằm trong phạm vi prototype UniSupport và các nội dung chưa thuộc phạm vi triển khai hiện tại.

**Acceptance Criteria**
- In-scope functions được liệt kê và liên kết với các module Student Portal, Staff Workspace, Management Dashboard và Security & Access.
- Out-of-scope items được ghi rõ, bao gồm các giới hạn đã thống nhất trong Project Proposal.
- Scope không mâu thuẫn với Functional Requirements và Master Plan.
- Các giới hạn của prototype, simulated data và production deployment được nêu rõ.
- Product Scope document được lưu và có thể truy xuất trong repository.

**Evidence**
`docs/01-product/product-scope.md` và Project Proposal.

## Issue #5 – Define User Roles and Permission Boundaries
**FR ID:** FR-SEC-01  
**Related AC:** FR-SEC-01/AC-01–AC-04  
**Related NFR:** NFR-SEC-01, NFR-SEC-02, NFR-SEC-03, NFR-SEC-04

**Description**
Xác định các Role chính của UniSupport và phạm vi chức năng, dữ liệu mà Student, Staff và Management được phép truy cập.

**Acceptance Criteria**
- Student, Staff và Management được mô tả với trách nhiệm và phạm vi sử dụng hệ thống.
- Permission Matrix xác định chức năng và dữ liệu được phép truy cập theo từng Role.
- Quyền truy cập Request của Student được giới hạn theo tài khoản sở hữu.
- Quyền truy cập Request của Staff được giới hạn theo Department hoặc phạm vi Assignment được cấp.
- Quyền truy cập Dashboard và báo cáo của Management được xác định theo quyền được cấp.
- Các trường hợp truy cập ngoài quyền được ghi nhận làm cơ sở kiểm thử.

**Evidence**
`docs/02-domain/users-and-roles.md`, M04 PRD và Role Permission Matrix.
**Scope note**
Không tự đưa chức năng Management tự quản lý/thay đổi Role vào scope đã chốt nếu FR-SEC-01/AC-05–AC-06 chưa được Sponsor xác nhận.

## Issue #6 – Requirements Baseline
**FR ID:** FR-STU-01, FR-STU-02, FR-STU-03, FR-STA-01, FR-STA-02, FR-STA-03, FR-MGT-01, FR-MGT-02, FR-SEC-01, FR-SEC-02  
**Related NFR:** NFR-PERF-01–03, NFR-USE-01–03, NFR-COMP-01–02, NFR-SEC-01–07, NFR-REL-01–04

**Description**
Tập hợp và baseline các Functional Requirements và Non-Functional Requirements của UniSupport làm cơ sở cho thiết kế, phát triển và kiểm thử prototype.

**Acceptance Criteria**
- Mười Functional Requirements hiện có được ghi nhận với Requirement ID duy nhất.
- Mỗi FR có mô tả, actor, priority, preconditions, main flow, business rules và acceptance criteria.
- Các Non-Functional Requirements có mã ID, cách đo và ngưỡng đánh giá hoặc trạng thái cần xác nhận.
- Các requirement chưa được Sponsor xác nhận được đánh dấu rõ, không tự xem là baseline đã duyệt.
- Requirements được đối chiếu với Product Scope, module PRDs và Workflows.
- Các thay đổi sau baseline được ghi nhận theo Change Control.

**Evidence**
Functional Requirements, Non-Functional Requirements, Product Scope và Traceability Matrix.

## Issue #7 – Define Request Status, Priority, and Business Rules
**FR ID:** FR-STU-02, FR-STA-01, FR-STA-02, FR-STA-03, FR-MGT-01  
**Related AC:** FR-STU-02/AC-02–AC-05; FR-STA-01/AC-02; FR-STA-02/AC-02–AC-05; FR-STA-03/AC-02, AC-05, AC-09, AC-11; FR-MGT-01/AC-03–AC-05  
**Related NFR:** NFR-USE-03, NFR-REL-02, NFR-REL-03

**Description**
Xác định danh mục Request Status, Priority, quy tắc chuyển trạng thái và các business rules ảnh hưởng đến việc tiếp nhận, phân công, xử lý và đóng Request.

**Acceptance Criteria**
- Danh mục Status được ghi nhận thống nhất trong `request-status.md`.
- Các chuyển trạng thái hợp lệ và không hợp lệ được mô tả rõ.
- Quy tắc chuyển sang trạng thái chờ bổ sung thông tin và quay lại xử lý được mô tả.
- Điều kiện đóng Request được xác định theo Workflow.
- Priority và quy tắc sử dụng Priority được mô tả nhất quán với FR-STA-01.
- Quy tắc xác định Request quá hạn được ghi nhận; thời gian xử lý mục tiêu chưa được Sponsor xác nhận phải được đánh dấu cần xác nhận.
- Business Rules và Workflows không mâu thuẫn với Functional Requirements.

**Evidence**
`request-status.md`, `business-rules.md` và workflow documents.

## Issue #8 – Review Acceptance Criteria and Requirement Traceability
**FR ID:** All current FRs: FR-STU-01–03, FR-STA-01–03, FR-MGT-01–02, FR-SEC-01–02  
**Related NFR:** All current NFRs

**Description**
Rà soát Acceptance Criteria và thiết lập khả năng truy xuất giữa Requirements, Acceptance Criteria, Test Scenarios, WBS tasks và Milestones.

**Acceptance Criteria**
- Mỗi FR-specific Acceptance Criterion giữ đúng mã được định nghĩa trong Functional Requirements.
- Các Test Scenarios tham chiếu đúng FR/AC hoặc NFR tương ứng.
- Traceability Matrix thể hiện Parent Task (WBS), Milestone và Test Scenario liên quan khi đã có thông tin.
- Các requirement chưa được xác nhận được đánh dấu TBD/Needs Confirmation.
- Các khoảng trống hoặc sai lệch traceability được ghi nhận để xử lý.
- Không tự tạo FR ID, AC ID hoặc Test Scenario ID chưa tồn tại trong tài liệu nguồn.

**Evidence**
`acceptance-criteria.md`, `test-scenarios.md`, `traceability-matrix.md`.

## Issue #9 – Document End-to-End Support Workflows
**FR ID:** FR-STU-01, FR-STU-02, FR-STU-03, FR-STA-01, FR-STA-02, FR-STA-03  
**Related AC:** Relevant FR-specific ACs and project-level AC-01–AC-10, AC-14

**Description**
Mô tả các workflow chính từ lúc Student gửi Request đến khi Staff xử lý, chuyển tiếp, giải quyết và Student gửi Feedback.

**Acceptance Criteria**
- WF-01 mô tả được luồng Submit Request.
- WF-02 mô tả được Classification and Assignment.
- WF-03 mô tả được Request Processing.
- WF-04 mô tả được Request Additional Information.
- WF-05 mô tả được Transfer Request.
- WF-06 mô tả được Resolve and Close.
- WF-07 mô tả được Feedback.
- Mỗi workflow xác định actor, preconditions, main flow, alternative/error flows và kết quả.
- Các workflow nhất quán với Request Status, Business Rules và Functional Requirements.

**Evidence**
`docs/04-workflows/WF-01` đến `WF-07`.

## Issue #10 – ERD
**FR ID:** FR-STU-01, FR-STU-02, FR-STU-03, FR-STA-01, FR-STA-02, FR-STA-03, FR-MGT-01, FR-MGT-02, FR-SEC-02  
**Related NFR:** NFR-PERF-03, NFR-REL-01, NFR-REL-02, NFR-REL-04

**Description**
Thiết kế Request Data Model và ERD để thể hiện các entity, thuộc tính và mối quan hệ dữ liệu cần thiết cho các workflow của UniSupport.

**Acceptance Criteria**
- ERD thể hiện các entity cần thiết để hỗ trợ Student, Staff, Department, Request, Assignment, Status History/Activity và Feedback theo data requirements.
- Các khóa chính, khóa ngoại và quan hệ giữa các entity được xác định.
- Request có định danh duy nhất và liên kết được với Student sở hữu.
- Assignment và lịch sử xử lý có thể truy xuất theo Request.
- Feedback có thể liên kết với Request tương ứng.
- Data Model hỗ trợ các truy vấn và báo cáo được yêu cầu trong phạm vi prototype.
- ERD nhất quán với Data Requirements và Functional Requirements.

**Evidence**
`docs/07-architecture/erd.md`, `data-requirements.md`, `request-model.md`.

## Issue #11 – Define System Architecture and Context
**FR ID:** All current FRs  
**Related NFR:** NFR-PERF-01–03, NFR-SEC-01–07, NFR-REL-01–04, NFR-COMP-01–02

**Description**
Xác định system context, các thành phần chính và cách các thành phần tương tác trong kiến trúc prototype UniSupport.

**Acceptance Criteria**
- System Context xác định Student, Staff, Management và các external entities liên quan.
- Architecture Overview mô tả các thành phần chính của prototype và trách nhiệm của từng thành phần.
- Luồng tương tác chính giữa frontend, backend và data storage được thể hiện ở mức phù hợp với prototype.
- Các điểm kiểm soát Authentication, Authorization và Data Access được xác định.
- Kiến trúc phù hợp với scope, assumptions và constraints của dự án.
- Architecture documents nhất quán với module PRDs và Data Requirements.

**Evidence**
`system-context.md`, `architecture-overview.md`.

## Issue #12 – Specify API Contracts and Data Requirements
**FR ID:** All current FRs  
**Related NFR:** NFR-PERF-01–03, NFR-SEC-01–05, NFR-REL-01–04

**Description**
Xác định API contracts và data requirements cần thiết để frontend và backend triển khai thống nhất các chức năng của UniSupport.

**Acceptance Criteria**
- Các API/use cases chính cho Submit Request, Tracking, Classification, Assignment, Processing, Transfer, Resolution, Feedback và Management Reporting được xác định.
- Mỗi API contract mô tả mục đích, actor/permission, input, output và lỗi chính ở mức phù hợp.
- Data Requirements xác định các trường dữ liệu cần thiết và quan hệ liên quan.
- Các API có kiểm tra quyền truy cập phù hợp với Role Permission Matrix.
- API contracts không mâu thuẫn với Functional Requirements, Workflows và ERD.
- Các nội dung chưa được quyết định được ghi rõ là TBD thay vì tự giả định.

**Evidence**
`data-requirements.md`, API contract documentation và Architecture Overview.

## Issue #13 – Review Student Portal, Staff Workspace, and Dashboard UI/UX
**FR ID:** FR-STU-01–03, FR-STA-01–03, FR-MGT-01–02, FR-SEC-01  
**Related NFR:** NFR-USE-01–03, NFR-COMP-01–02

**Description**
Rà soát UI/UX của Student Portal, Staff Workspace và Management Dashboard để bảo đảm giao diện hỗ trợ các workflow và Role tương ứng.

**Acceptance Criteria**
- Các màn hình chính của Student, Staff và Management được xác định.
- Mỗi màn hình có thể truy xuất đến workflow hoặc requirement liên quan.
- Các thao tác chính và thông tin cần hiển thị được thể hiện rõ.
- Request Status và hướng dẫn hành động được trình bày nhất quán.
- UI/UX không thể hiện chức năng nằm ngoài Product Scope đã chốt.
- Các màn hình được xem xét cho desktop/mobile và nội dung tiếng Việt/tiếng Anh theo NFR tương ứng.

**Evidence**
UI prototype, screen inventory và design review notes.

## Issue #14 – Prepare Client Prototype Review Session
**FR ID:** FR-STU-01, FR-STU-02, FR-SEC-01  
**Related AC:** FR-STU-01/AC-01–AC-03, FR-STU-02/AC-01–AC-03, AC-06, FR-SEC-01/AC-01, AC-04  
**Related NFR:** NFR-USE-01

**Description**
Chuẩn bị buổi review với client cho MS-01 prototype, tập trung vào việc Student đăng nhập, gửi Request và theo dõi Request.

**Acceptance Criteria**
- Mục tiêu và phạm vi review được xác định theo MS-01 deliverable.
- Kịch bản demo bao gồm các luồng Student Request Submission và Request Tracking đã sẵn sàng.
- Tài khoản và simulated data cần thiết được chuẩn bị.
- Các FR/AC sẽ được trình diễn và kiểm tra được liệt kê.
- Feedback questions và cách ghi nhận feedback được chuẩn bị.
- Không sử dụng dữ liệu cá nhân thật của sinh viên.

**Evidence**
Review agenda, demo script, test accounts và simulated data.

## Issue #15 – Conduct Client Prototype Acceptance Review
**FR ID:** FR-STU-01, FR-STU-02, FR-SEC-01  
**Related AC:** FR-STU-01/AC-01–AC-06, FR-STU-02/AC-01–AC-03, AC-06, FR-SEC-01/AC-01, AC-04  
**Related NFR:** NFR-USE-01, NFR-SEC-01–02

**Description**
Thực hiện review với client để xác minh MS-01 prototype đáp ứng các luồng Student Request Submission và Tracking đã thống nhất.

**Acceptance Criteria**
- Các kịch bản review được thực hiện trên prototype bằng simulated data.
- Kết quả từng tiêu chí được ghi nhận là Pass, Fail hoặc Blocked.
- Các lỗi hoặc điểm chưa đáp ứng được ghi lại kèm evidence.
- Client feedback và các câu hỏi chưa được giải quyết được ghi nhận.
- Các yêu cầu thay đổi phạm vi không được tự động đưa vào baseline; phải chuyển qua Change Control.
- Kết quả review được lưu trong repository.

**Evidence**
Review record, screenshots, test results và feedback notes.

## Issue #16 – Record Client Feedback and Update Product Backlog
**FR / NFR ID:** N/A – Client Feedback / Change Control

**Description**
Ghi nhận feedback từ client sau khi review MS-01 prototype, phân loại feedback và cập nhật Product Backlog theo quyết định đã thống nhất.

**Acceptance Criteria**
- Mỗi feedback có nội dung, nguồn/người gửi (nếu được phép ghi nhận), ngày nhận và module liên quan.
- Feedback được phân loại thành defect, clarification, enhancement hoặc change request khi phù hợp.
- Mỗi item có trạng thái xử lý và quyết định tiếp theo.
- Các thay đổi ảnh hưởng đến scope, schedule hoặc effort được đánh giá theo Change Control.
- Product Backlog được cập nhật và liên kết với issue tương ứng nếu đã tạo.
- Feedback chưa được chấp thuận không được xem là committed scope.

**Evidence**
Feedback log, updated Product Backlog và Change Log nếu có.

## Issue #17 – Authentication
**FR ID:** FR-SEC-01  
**Related AC:** FR-SEC-01/AC-01–AC-04  
**Related NFR:** NFR-SEC-01, NFR-SEC-07

**Description**
Triển khai cơ chế xác thực người dùng và áp dụng quyền truy cập cơ bản theo Role Student, Staff và Management trong prototype.

**Acceptance Criteria**
- Người dùng có thể đăng nhập bằng tài khoản giả lập hợp lệ được chuẩn bị cho prototype.
- Hệ thống xác định Role tương ứng sau khi người dùng đăng nhập.
- Student chỉ truy cập chức năng và dữ liệu dành cho Student.
- Staff chỉ truy cập chức năng và dữ liệu thuộc phạm vi được cấp.
- Management chỉ truy cập chức năng và dữ liệu được cấp.
- Hệ thống từ chối truy cập chức năng ngoài quyền của Role.
- Dữ liệu tài khoản dùng trong prototype/testing là dữ liệu giả lập.

**Evidence**
Authentication flow, role test accounts và permission test results.
**Scope note**
Issue này không mặc định bao gồm chức năng Management tạo tài khoản hoặc thay đổi Role; FR-SEC-01/AC-05–AC-06 đang cần xác nhận scope.

## Issue #18 – Request Submission
**FR ID:** FR-STU-01  
**Related AC:** FR-STU-01/AC-01–AC-06  
**Related NFR:** NFR-PERF-01, NFR-SEC-07

**Description**
Triển khai chức năng để Student tạo Request bằng cách chọn Request Type, nhập thông tin cần thiết và gửi biểu mẫu.

**Acceptance Criteria**
- Student đã đăng nhập có thể mở biểu mẫu Submit Request.
- Biểu mẫu cho phép nhập các trường thông tin và lựa chọn Request Type.
- Hệ thống không tạo Request khi thiếu trường bắt buộc và hiển thị thông tin cần bổ sung.
- Hệ thống tạo Request thành công với Request ID duy nhất.
- Student có thể gửi Request không có Attachment khi tài liệu không bắt buộc.
- Tệp không đáp ứng điều kiện được thông báo và không được tiếp nhận.
- Student nhận thông báo xác nhận sau khi Request được tiếp nhận.

**Evidence**
Prototype screenshots, request records và test results TS-001–TS-006.

## Issue #19 – Request Tracking
**FR ID:** FR-STU-02  
**Related AC:** FR-STU-02/AC-01–AC-03, AC-06  
**Related NFR:** NFR-SEC-02, NFR-PERF-01

**Description**
Triển khai chức năng để Student xem danh sách Request của mình, theo dõi Status hiện tại và xem lịch sử cập nhật.

**Acceptance Criteria**
- Student có thể xem danh sách Request thuộc tài khoản của mình.
- Status hiện tại của từng Request được hiển thị.
- Student có thể mở Request Detail và xem lịch sử cập nhật liên quan.
- Request chưa có lịch sử cập nhật được hiển thị với trạng thái/thông báo phù hợp.
- Student không thể xem Request thuộc tài khoản khác.
- Lỗi tải dữ liệu được thông báo và có hướng xử lý phù hợp.

**Evidence**
Student Portal screenshots, Request History records và test results TS-007–TS-009, TS-012.

## Issue #20 – Implement Request Classification and Assignment
**FR ID:** FR-STA-01  
**Related AC:** FR-STA-01/AC-01–AC-06  
**Related NFR:** NFR-SEC-03, NFR-REL-02

**Description**
Triển khai chức năng để Staff xem Request cần phân loại, xác định Request Type/Priority và phân công đến Department cùng người chịu trách nhiệm phù hợp.

**Acceptance Criteria**
- Staff có quyền phù hợp xem được các Request cần phân loại.
- Staff có thể xác định Request Type và Priority.
- Staff có thể chọn Department tiếp nhận phù hợp.
- Staff có thể chỉ định người chịu trách nhiệm.
- Hệ thống không xác nhận Assignment khi thiếu thông tin phân công bắt buộc.
- Các thay đổi Classification và Assignment được ghi nhận trong lịch sử.
- Staff không thể phân công Request cho tài khoản ngoài phạm vi hợp lệ.

**Evidence**
Staff Workspace screenshots, Assignment records và test results TS-019–TS-024.

## Issue #21 – Implement Staff Request Queue, Processing and Additional Information
**FR ID:** FR-STA-02, FR-STA-03, FR-STU-02, FR-STU-03  
**Related AC:** FR-STA-02/AC-01–AC-06; FR-STA-03/AC-01–AC-05, AC-10, AC-11; FR-STU-02/AC-05; FR-STU-03/AC-01–AC-02  
**Related NFR:** NFR-SEC-03, NFR-REL-02, NFR-REL-03

**Description**
Triển khai Staff Request Queue và các thao tác xử lý cơ bản, bao gồm xem Request được phân công, lọc danh sách, cập nhật Status, ghi Activity Log và yêu cầu Student bổ sung thông tin.

**Acceptance Criteria**
- Staff xem được Request thuộc phạm vi được phân công.
- Queue hiển thị Status, Priority và thời gian chờ của Request.
- Staff có thể lọc Request theo Status và Priority.
- Staff có thể xem nội dung và lịch sử xử lý của Request được phân công.
- Staff có thể cập nhật Status theo Status Flow đã thống nhất.
- Staff có thể ghi nhận nội dung xử lý vào Activity Log.
- Staff có thể yêu cầu Student bổ sung thông tin; Request chuyển sang trạng thái chờ bổ sung thông tin phù hợp.
- Student nhận thông báo khi Request cần bổ sung thông tin.
- Student có thể gửi thông tin bổ sung và hệ thống lưu vào đúng Request.
- Sau khi nhận đủ thông tin, Request có thể quay lại trạng thái xử lý theo quy trình.
- Staff không thể truy cập Request ngoài phạm vi được cấp.

**Evidence**
Staff Queue, Activity Log, notification records và test results TS-025–TS-035.
**Scope note**
Phần Additional Information thuộc MS-02 theo WBS 4.4 và Traceability Matrix; không gộp chức năng Transfer vào issue này.

## Issue #22 – Implement Request Transfer and Transfer History
**FR ID:** FR-STA-03  
**Related AC:** FR-STA-03/AC-06–AC-07  
**Related NFR:** NFR-REL-01, NFR-REL-02

**Description**
Triển khai chức năng để Staff chuyển Request sang Department khác khi cần, đồng thời bảo toàn thông tin và lịch sử xử lý trước khi chuyển.

**Acceptance Criteria**
- Staff có quyền phù hợp có thể chọn Department tiếp nhận mới.
- Hệ thống không hoàn tất Transfer nếu chưa xác định được Department tiếp nhận hợp lệ.
- Department/Assignment mới được ghi nhận trên Request.
- Request ID và nội dung Request được bảo toàn sau Transfer.
- Attachment và lịch sử xử lý trước Transfer được bảo toàn.
- Lịch sử ghi nhận việc Transfer và người thực hiện.
- Department/Staff nhận mới có thể truy cập Request theo quyền được cấp.

**Evidence**
Transfer records, before/after Request data và test results TS-036–TS-037, TS-078.

## Issue #23 – Implement Resolution, Closure, and Student Feedback
**FR ID:** FR-STA-03, FR-STU-03, FR-MGT-02  
**Related AC:** FR-STA-03/AC-09–AC-10; FR-STU-03/AC-03–AC-06; FR-MGT-02/AC-04  
**Related NFR:** NFR-REL-02, NFR-REL-03, NFR-REL-04

**Description**
Triển khai quy trình Staff ghi nhận kết quả giải quyết và đóng Request; Student có thể xem kết quả và gửi Feedback sau khi Request đủ điều kiện.

**Acceptance Criteria**
- Staff có thể cập nhật kết quả xử lý của Request được phân công.
- Hệ thống không cho phép đóng Request khi chưa đáp ứng điều kiện giải quyết.
- Thời điểm và người thực hiện hoạt động xử lý được ghi nhận.
- Student có thể xem kết quả xử lý của Request thuộc tài khoản mình.
- Student có thể gửi Feedback sau khi Request được giải quyết theo Workflow.
- Hệ thống từ chối Feedback khi Request chưa đủ điều kiện.
- Nội dung và thời điểm gửi Feedback được lưu và liên kết đúng Request.
- Feedback có thể được truy xuất để phục vụ Management Reporting.
- Student không thể gửi Feedback hoặc thao tác trên Request thuộc tài khoản khác.

**Evidence**
Resolution records, closed Request, Feedback records và test results TS-038 trở đi, TS-081.

## Issue #24 – Implement Management Dashboard and Reporting
**FR ID:** FR-MGT-01, FR-MGT-02  
**Related AC:** FR-MGT-01/AC-01–AC-06; FR-MGT-02/AC-01–AC-06  
**Related NFR:** NFR-PERF-02, NFR-PERF-03, NFR-SEC-04

**Description**
Triển khai Management Dashboard và các báo cáo tổng quan để Management theo dõi tình hình Request, Request quá hạn, hiệu suất xử lý và Feedback.

**Acceptance Criteria**
- Management có quyền phù hợp có thể truy cập Dashboard.
- Dashboard hiển thị số lượng Request mới và đang xử lý.
- Dashboard hiển thị danh sách/cảnh báo Request quá hạn dựa trên thời gian xử lý mục tiêu được cấu hình.
- Hệ thống hiển thị số liệu về thời gian xử lý Request.
- Hệ thống cung cấp thống kê Request theo Request Type.
- Hệ thống cung cấp workload theo Department.
- Hệ thống hiển thị dữ liệu Feedback phục vụ đánh giá chất lượng dịch vụ.
- Khi dữ liệu chưa đủ, hệ thống hiển thị thông báo phù hợp thay vì tạo số liệu không có căn cứ.
- Dữ liệu Dashboard/Report được đối chiếu với dữ liệu Request nguồn.
- Management không thể truy cập dữ liệu hoặc chức năng ngoài quyền được cấp.

**Evidence**
Dashboard screenshots, report outputs, simulated dataset và test results TS-041–TS-052, TS-063–TS-064.

## Issue #25 – Prepare MS-01 Test Scenarios from Acceptance Criteria
**FR ID:** FR-STU-01, FR-STU-02, FR-SEC-01  
**Related AC:** FR-STU-01/AC-01–AC-06; FR-STU-02/AC-01–AC-03, AC-06; FR-SEC-01/AC-01, AC-04  
**Related NFR:** NFR-PERF-01, NFR-USE-01, NFR-SEC-01–02, NFR-SEC-07

**Description**
Chuẩn bị Test Scenarios cho MS-01 để kiểm tra các chức năng Student Request Submission, Request Tracking và quyền truy cập liên quan.

**Acceptance Criteria**
- Test Scenarios bao phủ các FR/AC thuộc phạm vi MS-01.
- Mỗi Test Scenario có ID, preconditions, test data, steps và expected result.
- Có positive và negative scenarios cho các trường hợp chính.
- Có test case kiểm tra Student chỉ truy cập Request của tài khoản mình.
- Có test case kiểm tra dữ liệu giả lập và các NFR áp dụng cho MS-01.
- Test Scenarios được liên kết với FR/AC/NFR trong Traceability Matrix.
- Các ngưỡng Proposed baseline được đánh dấu là cần xác nhận trước khi dùng làm tiêu chí nghiệm thu chính thức.

**Evidence**
MS-01 Test Scenarios, test data và updated Traceability Matrix.

## Issue #26 – Test Role Permissions and Data Access Boundaries
**FR ID:** FR-SEC-01, FR-SEC-02  
**Related AC:** FR-SEC-01/AC-01–AC-04; FR-SEC-02/AC-01–AC-04  
**Related NFR:** NFR-SEC-01–05, NFR-SEC-07

**Description**
Kiểm thử quyền truy cập theo Role và khả năng bảo vệ dữ liệu Request, Attachment và Audit Log trên toàn hệ thống.

**Acceptance Criteria**
- Có test account giả lập cho Student, Staff và Management.
- Student không truy cập được Request/Attachment của Student khác.
- Staff không truy cập được Request ngoài Department hoặc Assignment scope được cấp.
- Management chỉ truy cập Dashboard, báo cáo và dữ liệu theo quyền được cấp.
- Các thao tác truy cập trái phép qua giao diện và direct URL/API (nếu có) bị từ chối.
- Các thay đổi quan trọng về Status, Priority, Assignment và hoạt động xử lý được ghi nhận theo FR-SEC-02.
- Audit Log chỉ được truy cập bởi Role có quyền phù hợp.
- Testing sử dụng dữ liệu giả lập, không sử dụng dữ liệu cá nhân thật.
- Các trường hợp liên quan NFR-SEC-06 được đánh dấu Blocked/Needs Confirmation nếu chưa có chính sách được Sponsor phê duyệt.

**Evidence**
Role Permission Matrix, security test results, screenshots/logs và defect records.

## Issue #27 – Run End-to-End Workflow and Regression Testing
**FR ID:** FR-STU-01–03, FR-STA-01–03, FR-MGT-01–02, FR-SEC-01–02  
**Related AC:** All applicable FR-specific ACs and project-level AC-01–AC-14  
**Related NFR:** All applicable NFRs, with approved/proposed status identified

**Description**
Thực hiện kiểm thử end-to-end cho các workflow chính và regression testing để xác minh các chức năng đã hoàn thành ở MS-01 đến MS-04 tiếp tục hoạt động sau các thay đổi tích hợp.

**Acceptance Criteria**
- Các workflow WF-01 đến WF-07 được kiểm thử theo thứ tự và điều kiện phù hợp.
- Luồng Submit → Classify → Assign → Process → Resolve → Feedback có thể được kiểm tra bằng simulated data.
- Các luồng Additional Information và Transfer được kiểm thử.
- Các chuyển Status hợp lệ được chấp nhận và chuyển Status không hợp lệ bị từ chối.
- Regression tests cho các chức năng đã bàn giao ở milestone trước được thực hiện.
- Mỗi Test Scenario có Actual Result và trạng thái Pass/Fail/Blocked/Not Run.
- Defects được ghi nhận với steps to reproduce, expected result, actual result và evidence.
- Không có defect nghiêm trọng chưa được xử lý làm gián đoạn workflow cốt lõi trước khi nghiệm thu.
- Các NFR chưa đủ điều kiện hoặc chưa được Sponsor xác nhận không bị đánh dấu Pass giả định.

**Evidence**
End-to-end test execution record, regression results, defect log và test evidence.

## Issue #28 – Validate Data Handling, Error Handling, and File Attachments
**FR ID:** FR-STU-01  
**Related AC:** FR-STU-01/AC-02, AC-04, AC-05  
**Related NFR:** NFR-SEC-07; NFR-REL-02 where applicable

**Description**
Kiểm tra việc validation dữ liệu đầu vào, xử lý lỗi khi gửi Request và quy tắc tiếp nhận Attachment trong Student Request Submission.

**Acceptance Criteria**
- Trường bắt buộc bị bỏ trống thì Request không được tạo.
- Dữ liệu chỉ chứa khoảng trắng trong trường bắt buộc được xử lý như dữ liệu không hợp lệ.
- Request Type không thuộc danh sách được hỗ trợ bị từ chối.
- Request không cần tài liệu bổ sung vẫn có thể được gửi khi Attachment không bắt buộc.
- Tệp không đáp ứng điều kiện được cấu hình bị từ chối và có thông báo phù hợp.
- Khi xảy ra lỗi validation, hệ thống không tạo Request không hợp lệ.
- Dữ liệu kiểm thử và dữ liệu prototype đều là dữ liệu giả lập.
- Kết quả kiểm tra được ghi nhận bằng test result và evidence.

**Evidence**
Validation test cases, screenshots, error messages và test records.

## Issue #29 – Document Test Results and Finalize Prototype
**FR / NFR ID:** All applicable FRs and NFRs covered by final testing

**Description**
Tổng hợp kết quả kiểm thử, ghi nhận defect còn lại và xác nhận trạng thái prototype trước khi thực hiện client acceptance.

**Acceptance Criteria**
- Kết quả kiểm thử được tổng hợp theo Test Scenario ID và FR/AC/NFR liên quan.
- Mỗi test có trạng thái Pass, Fail, Blocked hoặc Not Run.
- Các defect có mức độ ưu tiên, trạng thái xử lý và evidence.
- Các lỗi đã sửa được retest và kết quả retest được ghi nhận.
- Các known limitations và blocked items được liệt kê rõ.
- Traceability Matrix được cập nhật theo kết quả kiểm thử thực tế.
- Prototype được xác định trạng thái sẵn sàng hoặc chưa sẵn sàng cho client acceptance dựa trên bằng chứng, không chỉ dựa trên ngày hoàn thành.

**Evidence**
Test summary, defect log, updated Traceability Matrix và prototype release/version reference.

## Issue #30 – Prepare Client Acceptance Demonstration
**FR ID:** All in-scope FRs  
**Related AC:** Project-level AC-01–AC-14 in `acceptance-criteria.md`  
**Related NFR:** Applicable NFRs whose test status is available

**Description**
Chuẩn bị kịch bản trình diễn và nghiệm thu cuối với client, thể hiện các workflow chính và kết quả prototype đã kiểm thử.

**Acceptance Criteria**
- Demo agenda và demo script được chuẩn bị.
- Kịch bản demo bao phủ Student, Staff và Management.
- Các workflow Submit, Classify, Assign, Process, Transfer, Resolve, Close và Feedback được trình diễn theo phạm vi đã triển khai.
- Dashboard, báo cáo và quyền truy cập được trình diễn khi chức năng tương ứng đã sẵn sàng.
- Tài khoản và dữ liệu demo đều là dữ liệu giả lập.
- Các known limitations và out-of-scope items được trình bày rõ.
- Mỗi project-level Acceptance Criterion được ghi nhận kết quả review hoặc trạng thái chưa thể xác minh.
- Client feedback và acceptance decision được ghi lại.

**Evidence**
Demo script, test evidence, acceptance review record và client feedback.

## Issue #31 – Complete User Guide and Technical Documentation
**FR / NFR ID:** N/A – Supporting Deliverable for all in-scope modules

**Description**
Hoàn thiện User Guide và Technical Documentation để người dùng và nhóm tiếp nhận có thể hiểu cách sử dụng, cấu hình và duy trì prototype.

**Acceptance Criteria**
- User Guide mô tả các thao tác chính của Student, Staff và Management theo chức năng đã triển khai.
- Technical Documentation mô tả kiến trúc, cấu trúc dữ liệu và các thành phần kỹ thuật chính.
- Installation/configuration instructions được ghi rõ nếu thuộc phạm vi bàn giao.
- Tài liệu không hướng dẫn các chức năng chưa được triển khai như thể chúng đã sẵn sàng.
- Hình ảnh, tên chức năng và workflow trong tài liệu nhất quán với prototype hiện tại.
- Tài liệu được lưu trong repository và có thể truy cập.

**Evidence**
User Guide, Technical Documentation và Installation Guide.

## Issue #32 – Prepare Final Handover Package and Lessons Learned
**FR / NFR ID:** N/A – Supporting Deliverable / Project Handover

**Description**
Tập hợp các thành phần cần thiết để bàn giao prototype UniSupport và ghi nhận lessons learned của nhóm.

**Acceptance Criteria**
- Handover package có source code và hướng dẫn truy cập repository.
- Package có project documentation, User Guide và Technical Documentation.
- Package có Test Scenarios, test results và defect/known limitations records.
- Package có simulated seed data và hướng dẫn sử dụng dữ liệu nếu cần.
- Các cấu hình hoặc setup instructions cần thiết được ghi nhận, không đưa secret/password thật vào repository.
- Danh sách nội dung bàn giao được kiểm tra theo checklist.
- Lessons Learned ghi nhận các vấn đề, cách xử lý và đề xuất cải thiện.
- Handover review và trạng thái tiếp nhận được ghi lại.

**Evidence**
Handover checklist, repository links, documentation index và handover review record.

## Issue #33 – Prepare Database Schema and Simulated Seed Data
**FR ID:** FR-STU-01, FR-STU-02, FR-STU-03, FR-STA-01, FR-STA-02, FR-STA-03, FR-MGT-01, FR-MGT-02, FR-SEC-02  
**Related NFR:** NFR-PERF-03, NFR-SEC-07, NFR-REL-01, NFR-REL-02, NFR-REL-04

**Description**
Chuẩn bị database schema và simulated seed data để hỗ trợ phát triển, trình diễn và kiểm thử các workflow UniSupport.

**Acceptance Criteria**
- Database schema nhất quán với ERD và Data Requirements đã thống nhất.
- Các entity và quan hệ cần thiết cho Request, User/Role, Department, Assignment, Status History/Activity, Attachment metadata và Feedback được thể hiện theo scope.
- Seed data có các Role Student, Staff và Management.
- Seed data có Request với nhiều Request Type, Status, Priority và Assignment để phục vụ test.
- Seed data hỗ trợ các trường hợp Transfer, Resolution và Feedback.
- Dữ liệu được tạo là dữ liệu giả lập; không chứa dữ liệu cá nhân thật của sinh viên.
- Database có thể được khởi tạo từ hướng dẫn hoặc script được lưu trong repository.
- Dữ liệu mẫu có thể được truy vấn và đối chiếu với dữ liệu nguồn đã chuẩn bị.

**Evidence**
Schema/migration files, seed scripts, ERD và data validation results.

## Issue #34 – Refine Responsive Layout and Vietnamese-English UI Text
**FR ID:** All UI-related in-scope FRs  
**Related NFR:** NFR-COMP-01, NFR-COMP-02, NFR-USE-03

**Description**
Hoàn thiện khả năng hiển thị responsive và nội dung tiếng Việt/tiếng Anh trên các màn hình chính của prototype.

**Acceptance Criteria**
- Các màn hình thuộc workflow chính được kiểm tra ở desktop viewport 1366 × 768 và mobile viewport 360 × 800 theo Proposed baseline.
- Các thành phần chức năng chính không bị che khuất hoặc tràn ngang gây cản trở thao tác.
- Các thao tác chính vẫn thực hiện được trên desktop và mobile viewport.
- Nội dung tiếng Việt và tiếng Anh trong phạm vi đã thống nhất được hiển thị đầy đủ.
- Request Status labels nhất quán với `request-status.md`.
- Các màn hình yêu cầu Student hành động có hướng dẫn rõ ràng.
- Các lỗi giao diện được ghi nhận và retest sau khi sửa.
- Kích thước viewport là Proposed baseline, cần được xác nhận trước khi xem là điều kiện nghiệm thu chính thức.

**Evidence**
Responsive screenshots, language review checklist và UI regression results.

## Issue #35 – Validate Usability and Project Outcome KPIs
**FR / NFR ID:** NFR-USE-01, NFR-USE-02, NFR-USE-03; project outcome metrics where approved

**Description**
Đánh giá usability của các tác vụ chính và tổng hợp các chỉ số kết quả dự án dựa trên prototype, simulated data và kết quả kiểm thử.

**Acceptance Criteria**
- Các tác vụ Student gửi Request và theo dõi Request được đưa vào usability evaluation.
- Các tác vụ Staff tìm Request, cập nhật Status và ghi nhận hoạt động xử lý được đưa vào usability evaluation.
- Tỷ lệ hoàn thành độc lập, nhu cầu trợ giúp và lỗi thao tác được ghi nhận cho từng tác vụ.
- Các ngưỡng NFR-USE-01 và NFR-USE-02 được ghi là Proposed baseline cho đến khi được xác nhận.
- NFR-USE-03 được kiểm tra bằng cách đối chiếu Status labels và hướng dẫn bổ sung thông tin với domain/workflow documents.
- Các KPI dự án được định nghĩa cùng công thức đo, nguồn dữ liệu, thời điểm đo và kết quả thực tế.
- KPI target chưa được Sponsor/nhóm xác nhận không được tự đặt hoặc trình bày như mục tiêu đã phê duyệt.
- Kết quả usability và KPI được tổng hợp thành báo cáo, nêu rõ giới hạn của prototype và simulated data.

**Evidence**
Usability test records, KPI measurement sheet và evaluation summary.
**Source limitation**
`docs/10-product-management/success-metrics.md` hiện đang rỗng trong ZIP được cung cấp. Vì vậy, KPI cụ thể và target chưa thể được xác nhận từ tài liệu nguồn; cần bổ sung/duyệt trước khi chốt.

---

# Cross-checks before updating GitHub

## A. Recommended title alignment
- #17: Consider restoring the fuller title `Implement Role-Based Authentication and Access Control` rather than the one-word title `Authentication`.
- #18: `Implement Student Request Submission` is clearer than `Request Submission`.
- #19: `Implement Request Tracking and Timeline` is clearer than `Request Tracking`.
- #21: Rename to `Implement Staff Request Queue, Processing and Additional Information`.
- #22: Rename to `Implement Request Transfer and Transfer History`.
- #4: `Finalize Product Scope and Out-of-Scope Boundaries` is clearer than `Product Scope`.
- #6: `Baseline Functional and Non-Functional Requirements` is clearer than `Requirements Baseline`.
- #10: `Design Request Data Model and ERD` is clearer than `ERD`.
- #1: `Set Up Repository Workflow and Contribution Rules` is clearer than `Repository Setup`.

## B. Mapping concerns to reconcile
- Current Issue #21 and #22 titles overlap on Additional Information. The WBS places Student Notification & Additional Information in MS-02 (WBS 4.4), while Transfer is in MS-03 (WBS 5.1). The proposed title/scope above separates them without deleting either issue.
- Current Traceability Matrix maps FR-STU-03/AC-01–AC-02 to MS-02 and FR-STU-03/AC-03–AC-06 to MS-03. Keep that split in schedule/test planning even though Issue #21 now includes the first two ACs.
- Current Traceability Matrix maps FR-STU-02/AC-04–AC-05 to MS-02; Issue #19 (MS-01) should only claim Tracking AC-01–AC-03 and AC-06. Notification behavior belongs with MS-02.
- FR-SEC-01/AC-05–AC-06 (Management user/Role management) are marked as requiring scope confirmation in Traceability Matrix. Do not include them as committed acceptance criteria unless approved.
- NFR-SEC-06 (Data Retention/Data Handling Policy) is awaiting Sponsor confirmation. Do not invent retention periods or mark this requirement passed without an approved policy.
- `docs/10-product-management/success-metrics.md` is empty in the supplied ZIP. Issue #35 must define/confirm KPIs before targets can be treated as approved.
- The generic project-level AC-01–AC-14 in `acceptance-criteria.md` and the FR-specific AC IDs are different ID systems. Keep the source distinction in Issues #15, #27, #30 and the Traceability Matrix.

## C. Suggested issue body format
For each GitHub issue, keep:
1. `FR / NFR ID`
2. `Description`
3. `Acceptance Criteria`
4. `Evidence`
5. `Related Documents` (add exact repository paths when confirming the final location)

Do not add an Owner or Due date by guessing. Use the approved RACI/Resources and WBS schedule.
