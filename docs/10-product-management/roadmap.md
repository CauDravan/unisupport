# Product Roadmap

## 1. Roadmap Overview

Product Roadmap mô tả các **Product Increments** mà UniSupport hướng đến cung cấp cho Student, Staff và Management. Roadmap tập trung vào giá trị và khả năng sử dụng của từng phần sản phẩm, không mô tả các hoạt động nội bộ của môn học hoặc các giai đoạn hành chính như presentation/review.

UniSupport hiện được xây dựng dưới dạng prototype với Simulated Data. Các mốc thời gian dưới đây đồng bộ với bốn Milestones trong [Master Plan](../08-project/master-plan.md); ngày bắt đầu dự án trong Master Plan hiện vẫn là giả định tạm thời. `master-plan.xlsx` là nguồn chính thức để quản lý lịch trình chi tiết.

## 2. Product Increments

### Increment 1 – Student Request Submission & Tracking

**Target Milestone:** MS-01  
**Planned Completion:** 15/01/2027  
**Primary Users:** Student

Sinh viên có thể gửi Request qua Student Portal, cung cấp Request Type, Subject, Description và Attachment nếu cần. Hệ thống tiếp nhận Request, tạo Request ID và cho phép Student xem danh sách, chi tiết, Status cùng thông tin cập nhật phù hợp.

**Expected Product Outcome:** Student có thể gửi yêu cầu và tự theo dõi tình trạng yêu cầu đã gửi thay vì phải hỏi thủ công để biết hệ thống đã tiếp nhận hay chưa.

**Acceptance Evidence:** Demonstrate Student Request Submission và Request Tracking; kiểm tra các Acceptance Criteria và Test Scenarios liên quan đến FR-STU; xác minh Request ID, dữ liệu Request và Status hiển thị đúng.

### Increment 2 – Staff Request Classification & Processing

**Target Milestone:** MS-02  
**Planned Completion:** 29/01/2027  
**Primary Users:** Staff

Staff có thể xem Request trong phạm vi được cấp, phân loại Request, xác định Department/Assigned Staff và Priority, sau đó cập nhật Status và ghi nhận hoạt động xử lý. Các yêu cầu cần thêm thông tin có thể được chuyển sang trạng thái chờ Student bổ sung theo Workflow đã xác định.

**Expected Product Outcome:** Request có nơi chịu trách nhiệm rõ ràng và Staff có thể thực hiện các bước xử lý theo quy trình thống nhất.

**Acceptance Evidence:** Demonstrate Request Classification & Assignment và các hoạt động Request Processing; kiểm tra Assignment, Status transition, Request History và quyền truy cập theo các FR/AC/TS liên quan.

### Increment 3 – Request Transfer, Resolution & Feedback

**Target Milestone:** MS-03  
**Planned Completion:** 12/02/2027  
**Primary Users:** Student and Staff

Staff có thể Transfer Request sang Staff hoặc Department khác khi cần, giữ lại thông tin và lịch sử xử lý, ghi nhận kết quả giải quyết và đóng Request theo Workflow. Student có thể gửi Feedback sau khi Request được xử lý/đóng theo điều kiện của quy trình.

**Expected Product Outcome:** Quá trình bàn giao, giải quyết và phản hồi được ghi nhận xuyên suốt; Request không mất lịch sử khi chuyển người/bộ phận phụ trách.

**Acceptance Evidence:** Demonstrate Transfer, Resolution, Closure và Feedback; kiểm tra Request ID, Assignment mới, lịch sử xử lý, Status và liên kết Feedback với Request tương ứng.

### Increment 4 – Management Dashboard, Security & Handover

**Target Milestone:** MS-04  
**Planned Completion:** 26/02/2027  
**Primary Users:** Management; all roles for access control

Management có thể xem Dashboard và báo cáo tổng hợp về Request, Status, Request quá hạn, hiệu quả xử lý, Request Type phổ biến và Feedback. Các chức năng được bảo vệ theo Role; hoạt động quan trọng được ghi nhận theo yêu cầu. Prototype, Simulated Data, tài liệu và bằng chứng kiểm thử được chuẩn bị cho việc bàn giao.

**Expected Product Outcome:** Management có thông tin tổng quan để theo dõi hoạt động hỗ trợ; các vai trò chỉ truy cập dữ liệu/chức năng trong phạm vi được cấp; nhóm tiếp nhận có tài liệu để hiểu và kiểm tra prototype.

**Acceptance Evidence:** Demonstrate Management Dashboard và reports; thực hiện các kiểm thử Role-based Access, Student Data Protection và Audit Logging; xác minh regression tests và bộ tài liệu bàn giao theo Quality Plan.

## 3. Roadmap Summary

| Product Increment | Main Capability | Milestone | Planned Completion |
|---|---|---|---|
| Increment 1 | Student Request Submission & Tracking | MS-01 | 15/01/2027 |
| Increment 2 | Staff Request Classification & Processing | MS-02 | 29/01/2027 |
| Increment 3 | Request Transfer, Resolution & Feedback | MS-03 | 12/02/2027 |
| Increment 4 | Management Dashboard, Security & Handover | MS-04 | 26/02/2027 |

## 4. Prioritization and Roadmap Changes

Thứ tự các Product Increments phản ánh bốn Milestones hiện có trong Master Plan và sự phụ thuộc nghiệp vụ giữa việc tiếp nhận Request, xử lý Request, hoàn tất/Feedback và báo cáo quản lý. Product Backlog được sử dụng để theo dõi các chức năng chi tiết và Priority.

Roadmap không tự tạo cam kết mới. Khi có Feedback hoặc đề xuất thay đổi:

1. Ghi nhận và phân loại theo [Feedback Process](./feedback-process.md).
2. Đánh giá giá trị sản phẩm, Product Scope, dependencies, effort và ảnh hưởng đến các Milestones.
3. Nếu thay đổi ảnh hưởng đến baseline về scope, schedule, effort, resources hoặc deliverables, thực hiện Change Control trong Master Plan và xin phê duyệt theo Project Governance.
4. Chỉ cập nhật Roadmap và các tài liệu liên quan sau khi quyết định được xác nhận; đồng bộ Product Backlog, WBS, GitHub Issues và Acceptance/Testing artifacts.

## 5. Future Considerations

Các chức năng hoặc thay đổi chưa nằm trong bốn Product Increments hiện tại có thể được ghi nhận trong Product Backlog hoặc Future Considerations để xem xét sau. Việc xuất hiện trong danh sách này không đồng nghĩa với cam kết triển khai trong project hiện tại. Mọi nội dung cần được đánh giá theo Product Scope, thời gian 15 tuần, giới hạn 320 person-hours và quyết định của Project Sponsor / Simulated Client.

## 6. Related Documents

- [Product Goals](../01-product/product-goals.md)
- [Product Scope](../01-product/product-scope.md)
- [Product Backlog](../01-product/product-backlog.md)
- [Module PRDs](../03-modules/README.md)
- [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)
- [WF-02 – Classify and Assign](../04-workflows/WF-02-classify-and-assign.md)
- [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)
- [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- [WF-05 – Transfer Request](../04-workflows/WF-05-transfer-request.md)
- [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)
- [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)
- [Functional Requirements](../05-requirements/functional-requirements.md)
- [Acceptance Criteria](../06-acceptance/acceptance-criteria.md)
- [Test Scenarios](../06-acceptance/test-scenarios.md)
- [Master Plan](../08-project/master-plan.md)
- [Feedback Process](./feedback-process.md)
- [Success Metrics](./success-metrics.md)
