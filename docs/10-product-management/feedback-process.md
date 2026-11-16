# Feedback Process

## 1. Purpose

Tài liệu này quy định cách nhóm UniSupport tiếp nhận, ghi nhận, phân loại, đánh giá và theo dõi Feedback trong quá trình phát triển prototype. Quy trình giúp bảo đảm ý kiến của Student, Staff, Management và Project Sponsor không bị bỏ sót, đồng thời phân biệt Feedback thông thường với Bug và Change Request.

UniSupport hiện được thực hiện trong bối cảnh **Simulated Client**. Các vai trò và quyết định được mô tả trong tài liệu này là quy trình quản lý của dự án mô phỏng; không được hiểu là Aurora University đã chính thức phê duyệt.

## 2. Feedback Sources

Feedback có thể được ghi nhận từ các nguồn sau:

| Source | Nội dung có thể ghi nhận |
|---|---|
| Student | Khó khăn khi gửi Request, theo dõi Status, bổ sung thông tin hoặc gửi Feedback. |
| Staff | Khó khăn khi phân loại, Assignment, xử lý, Transfer hoặc cập nhật Request. |
| Management | Ý kiến về Dashboard, Overdue Request, báo cáo và thông tin quản lý. |
| Project Sponsor / Simulated Client | Nhận xét về Product Scope, kết quả bàn giao, mức độ phù hợp với mục tiêu và các thay đổi được đề xuất. |
| Project Team | Vấn đề phát hiện trong Prototype Demonstration, Test Scenarios, Usability Testing hoặc quá trình rà soát tài liệu. |

## 3. Feedback Intake and Recording

1. Người tiếp nhận ghi lại Feedback bằng một GitHub Issue hoặc bản ghi có thể truy vết trong project repository.
2. Nội dung cần ghi nhận gồm: mô tả vấn đề/đề xuất, người hoặc nhóm đưa ra ý kiến (nếu xác định được), ngày tiếp nhận, module/workflow liên quan, ảnh chụp hoặc bước tái hiện nếu có, và kết quả mong đợi.
3. Nếu Feedback phát sinh trong buổi trao đổi hoặc trình diễn, nhóm ghi lại nội dung và xác nhận lại cách hiểu với người đưa ra ý kiến khi cần.
4. Không tự xem một ý kiến là yêu cầu đã được chấp thuận hoặc cam kết triển khai.

Thông tin cá nhân thật của sinh viên không được đưa vào Feedback record hoặc dữ liệu prototype. Khi cần minh họa, sử dụng Simulated Data.

## 4. Feedback Classification

Mỗi bản ghi được phân loại theo bản chất chính:

| Type | Meaning | Handling |
|---|---|---|
| Bug | Chức năng hiện tại hoạt động khác với Functional Requirements, Business Rules hoặc Acceptance Criteria đã thống nhất. | Ghi nhận bước tái hiện, kết quả thực tế/mong đợi, mức độ ảnh hưởng và liên kết Test Scenario nếu có. |
| Product Feedback | Ý kiến về mức độ dễ sử dụng, nội dung hiển thị hoặc giá trị của chức năng hiện có. | Đánh giá tác động đến người dùng và Product Goals; xem xét cập nhật Product Backlog. |
| Change Request (CR) | Đề xuất thay đổi Product Scope, Functional Requirements, deliverable, schedule, effort hoặc resource đã baseline. | Chuyển qua Change Control; không tự triển khai trước khi được phê duyệt. |
| Question / Clarification | Câu hỏi hoặc nội dung chưa rõ về yêu cầu, quy trình hay cách sử dụng. | Làm rõ với nguồn phù hợp và cập nhật tài liệu nếu có quyết định được xác nhận. |

Nếu một Feedback vừa mô tả Bug vừa đề xuất chức năng mới, nhóm tạo liên kết giữa Bug và Change Request thay vì gộp hai vấn đề thành một kết luận.

## 5. Assessment and Prioritization

Nhóm xem xét từng Feedback theo các tiêu chí:

- **User Impact:** Mức độ ảnh hưởng đến Student, Staff hoặc Management.
- **Goal and Scope Alignment:** Mức độ đóng góp cho Product Goals và sự phù hợp với Product Scope.
- **Severity / Risk:** Mức độ ảnh hưởng đến dữ liệu, quyền truy cập, tính đúng đắn hoặc khả năng hoàn thành workflow.
- **Dependencies:** Các chức năng, Workflow, FR hoặc module phụ thuộc.
- **Effort and Feasibility:** Effort dự kiến và khả năng thực hiện trong giới hạn 15 tuần, tối đa 320 person-hours.

Priority sử dụng định nghĩa High, Medium và Low trong [Product Backlog](../01-product/product-backlog.md). Nhóm không tự đặt trọng số hoặc công thức chấm điểm khi chưa có cơ sở được thống nhất.

| Priority | Handling |
|---|---|
| High | Xem xét trước vì ảnh hưởng đến chức năng cốt lõi, bảo mật, dữ liệu hoặc điều kiện nghiệm thu. |
| Medium | Xếp vào Product Backlog để cân nhắc theo giá trị, phụ thuộc và nguồn lực. |
| Low | Có thể xem xét sau khi các hạng mục quan trọng hơn đã được đáp ứng; không mặc nhiên thuộc cam kết hiện tại. |

## 6. Review, Decision and Implementation

1. **Initial Review:** Project team kiểm tra bản ghi có đủ thông tin, xác định loại Feedback và tài liệu liên quan.
2. **Impact Assessment:** Nhóm đánh giá ảnh hưởng đến Product Scope, FR/NFR, Acceptance Criteria, WBS, schedule, effort, quotation và các Test Scenarios liên quan.
3. **Decision:**
   - Bug được xử lý theo mức độ ảnh hưởng và Quality Plan, trong phạm vi yêu cầu đã thống nhất.
   - Product Feedback được xem xét để cập nhật hoặc sắp xếp lại Product Backlog.
   - Change Request ảnh hưởng đến scope, mục tiêu, lịch trình, effort, nguồn lực hoặc deliverables phải được Project Sponsor / Simulated Client xem xét và chấp thuận trước khi baseline thay đổi.
   - Nội dung chưa đủ thông tin hoặc chưa được xác nhận được giữ trạng thái Open / Needs Clarification; không tự suy diễn thành quyết định.
4. **Implementation:** Chỉ đưa hạng mục đã được lựa chọn vào công việc thực hiện; liên kết GitHub Issue với PBI, FR, MS-xx và Test Scenario có liên quan khi áp dụng.
5. **Verification and Closure:** Kiểm tra kết quả theo Acceptance Criteria hoặc điều kiện đã thống nhất; cập nhật trạng thái Issue và đóng bản ghi khi có bằng chứng hoàn thành.

Project Manager điều phối việc ghi nhận và theo dõi. Project team thực hiện phân tích và đề xuất ưu tiên. Thẩm quyền Product Owner lâu dài sau bàn giao chưa được xác định trong nguồn dự án và cần Client xác nhận; không mặc định nhóm sinh viên có quyền quyết định thay Aurora University.

## 7. Change Control Boundary

Feedback không tự động làm thay đổi baseline. Với CR ảnh hưởng đến Product Scope, schedule, effort, resources hoặc deliverables, nhóm thực hiện quy trình trong [Master Plan](../08-project/master-plan.md): ghi nhận CR, đánh giá tác động, xin phê duyệt, cập nhật Change Log và đồng bộ tài liệu/GitHub sau khi được chấp thuận.

Các đề xuất chưa được duyệt có thể được lưu trong Product Backlog hoặc Future Consideration, nhưng phải thể hiện rõ trạng thái chưa cam kết.

## 8. Feedback Record Fields

Mỗi Feedback record nên có tối thiểu các trường sau:

| Field | Description |
|---|---|
| Feedback ID / Issue ID | Mã nhận diện để truy vết. |
| Date Received | Ngày tiếp nhận. |
| Source | Nhóm người dùng hoặc nguồn cung cấp. |
| Type | Bug, Product Feedback, Change Request hoặc Question / Clarification. |
| Description | Nội dung cụ thể và bối cảnh. |
| Related Module / Workflow / FR | Phạm vi bị ảnh hưởng. |
| Priority / Severity | Mức độ ưu tiên hoặc ảnh hưởng sau khi đánh giá. |
| Decision and Rationale | Quyết định và lý do; ghi rõ nếu còn chờ xác nhận. |
| Owner / Status | Người theo dõi và trạng thái xử lý. |
| Verification Evidence | Test Scenario, kết quả kiểm tra hoặc liên kết PR khi có. |

## 9. Related Documents

- [Product Backlog](../01-product/product-backlog.md)
- [Product Scope](../01-product/product-scope.md)
- [Functional Requirements](../05-requirements/functional-requirements.md)
- [Acceptance Criteria](../06-acceptance/acceptance-criteria.md)
- [Test Scenarios](../06-acceptance/test-scenarios.md)
- [Quality Plan](../09-quality/quality-plan.md)
- [Master Plan](../08-project/master-plan.md)
- [Project Governance](../11-governance/project-governance.md)
