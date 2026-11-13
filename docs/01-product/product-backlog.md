# Product Backlog

## 1. Purpose

Product Backlog là danh sách các chức năng và yêu cầu dự kiến được phát triển cho UniSupport. Tài liệu giúp xác định những nội dung cần có trong sản phẩm, giá trị mà từng hạng mục mang lại và mức độ ưu tiên tương đối khi xem xét triển khai.

Product Backlog được xây dựng dựa trên:

- Product Goals.
- Product Scope.
- Functional Requirements.
- Non-Functional Requirements.
- Acceptance Criteria.
- Feedback từ Client và các Stakeholders.

Product Backlog được sử dụng để theo dõi các chức năng cần phát triển, hỗ trợ việc sắp xếp thứ tự ưu tiên và điều chỉnh phạm vi sản phẩm khi có thay đổi được xem xét và chấp thuận.

## 2. Product Backlog Management

Product Backlog được quản lý và cập nhật trong suốt quá trình phát triển UniSupport.

Các nguyên tắc quản lý bao gồm:

- Mỗi Product Backlog Item (PBI) phải mô tả rõ chức năng cần có và giá trị dự kiến mang lại.
- Mỗi PBI cần có Priority và liên kết với Functional Requirements hoặc các tài liệu nghiệp vụ liên quan.
- Các PBI phải phù hợp với Product Scope và Project Goals.
- Feedback từ Client và Stakeholders phải được ghi nhận, phân loại và đánh giá trước khi đưa vào Product Backlog.
- Priority có thể được điều chỉnh khi có thay đổi về nhu cầu, giá trị sản phẩm, phạm vi hoặc nguồn lực.
- Các chức năng được lựa chọn triển khai phải phù hợp với giới hạn thời gian 15 tuần và ngân sách lao động tối đa 320 person-hours.
- GitHub Issues được sử dụng để theo dõi các công việc cụ thể liên quan đến từng PBI.

Việc cập nhật Product Backlog không đồng nghĩa với việc một chức năng đã được phê duyệt để triển khai. Những thay đổi ảnh hưởng đến Project Scope, effort hoặc kế hoạch cần được xem xét và chấp thuận theo quy trình Change Control.

## 3. Priority Definitions

Priority được sử dụng để xác định mức độ quan trọng tương đối của từng Product Backlog Item.

| Priority | Description |
|---|---|
| High | Chức năng cốt lõi hoặc cần thiết để đáp ứng Mandatory Project Scope và các mục tiêu chính của UniSupport. Cần được ưu tiên xem xét triển khai. |
| Medium | Chức năng bổ sung giá trị cho người dùng và hỗ trợ cải thiện hoạt động của hệ thống, nhưng không phải chức năng có mức độ ưu tiên cao nhất. |
| Low | Chức năng có thể xem xét trong giai đoạn sau khi các chức năng quan trọng hơn đã được đáp ứng và còn thời gian, nguồn lực phù hợp. |

### 3.1. Priority Evaluation Criteria

Khi đánh giá hoặc thay đổi Priority, nhóm xem xét các yếu tố sau:

- **Business Value:** Mức độ đóng góp của chức năng đối với Project Goals và nhu cầu của người dùng.
- **Scope Importance:** Mức độ cần thiết để đáp ứng Mandatory Project Scope.
- **User Impact:** Mức độ ảnh hưởng đến Student, Staff và Management.
- **Dependencies:** Mức độ phụ thuộc của chức năng vào các chức năng hoặc yêu cầu khác.
- **Effort and Feasibility:** Effort dự kiến và khả năng thực hiện trong giới hạn nguồn lực của dự án.

Các tiêu chí trên được sử dụng để hỗ trợ việc đánh giá và sắp xếp thứ tự ưu tiên. Hiện chưa có trọng số hoặc công thức Priority Scoring được Client xác nhận.

## 4. Product Backlog Items

Product Backlog hiện tại bao gồm 13 hạng mục, được chia theo bốn module chính của UniSupport.

### 4.1. Student Portal

| ID | Product Backlog Item | Description | Expected Value | Priority | Related Requirements |
|---|---|---|---|---|---|
| PBI-01 | User Authentication | Cho phép người dùng truy cập hệ thống bằng tài khoản phù hợp với vai trò được cấp. | Hỗ trợ xác thực người dùng và kiểm soát quyền truy cập vào hệ thống. | High | FR-SEC-01 |
| PBI-02 | Student Request Submission | Cho phép Student tạo và gửi yêu cầu hỗ trợ bằng cách cung cấp Request Type, Subject, Description và tài liệu đính kèm nếu cần. Hệ thống tạo Request ID và xác nhận khi yêu cầu được tiếp nhận thành công. | Giúp Student gửi yêu cầu tập trung, hạn chế việc yêu cầu bị bỏ sót và cung cấp thông tin cần thiết cho quá trình xử lý. | High | FR-STU-01, WF-01, AC-01, AC-02 |
| PBI-03 | Request Tracking | Cho phép Student xem danh sách yêu cầu đã gửi, trạng thái hiện tại, lịch sử xử lý và nhận thông báo khi có cập nhật liên quan đến yêu cầu. | Giúp Student chủ động theo dõi tiến độ và giảm số lần phải liên hệ để hỏi tình trạng xử lý. | Medium | FR-STU-02, WF-01, WF-06, AC-10 |
| PBI-07 | Additional Information Handling | Cho phép Staff yêu cầu Student bổ sung thông tin và ghi nhận thông tin được cung cấp. | Giúp Staff có đủ thông tin để tiếp tục xử lý yêu cầu và hạn chế việc trao đổi thông tin qua nhiều kênh. | Medium | FR-STU-03, FR-STA-03, WF-04, AC-06, AC-07 |

### 4.2. Staff Workspace

| ID | Product Backlog Item | Description | Expected Value | Priority | Related Requirements |
|---|---|---|---|---|---|
| PBI-04 | Request Classification | Cho phép Staff xem xét và phân loại yêu cầu theo nhóm phù hợp dựa trên nội dung và Request Type. | Giúp yêu cầu được xác định đúng loại và chuyển đến bộ phận phù hợp. | High | FR-STA-01, WF-02 |
| PBI-05 | Request Assignment | Cho phép Staff phân công yêu cầu cho người hoặc bộ phận phụ trách. | Bảo đảm yêu cầu có người chịu trách nhiệm rõ ràng, hạn chế tình trạng bị bỏ sót hoặc xử lý trùng lặp. | High | FR-STA-01, WF-02, AC-03, AC-04 |
| PBI-06 | Request Processing | Cho phép Staff xem các yêu cầu được giao, cập nhật trạng thái, ghi nhận hoạt động xử lý và chuyển yêu cầu sang Staff hoặc Department khác khi cần thiết. | Hỗ trợ Staff phối hợp xử lý yêu cầu theo quy trình thống nhất và duy trì lịch sử xử lý. | High | FR-STA-02, FR-STA-03, WF-03, WF-05, AC-05, AC-08 |
| PBI-08 | Request Resolution & Closure | Cho phép Staff ghi nhận kết quả xử lý và hoàn tất yêu cầu theo quy trình. | Bảo đảm mỗi yêu cầu có kết quả xử lý được ghi nhận và trạng thái hoàn tất rõ ràng. | High | FR-STA-03, WF-06, AC-09 |

### 4.3. Management Dashboard

| ID | Product Backlog Item | Description | Expected Value | Priority | Related Requirements |
|---|---|---|---|---|---|
| PBI-10 | Management Dashboard | Cung cấp Dashboard giúp Management theo dõi số lượng yêu cầu mới, yêu cầu đang xử lý, yêu cầu quá hạn và các cảnh báo liên quan. | Giúp Management nhận biết tình hình xử lý và các yêu cầu cần được theo dõi hoặc can thiệp. | Medium | FR-MGT-01, AC-11 |
| PBI-11 | Management Reporting | Cho phép Management xem báo cáo về thời gian xử lý trung bình, loại yêu cầu phổ biến, khối lượng công việc theo Department và dữ liệu Feedback của Student. | Cung cấp dữ liệu hỗ trợ Management đánh giá chất lượng dịch vụ và nhận biết các vấn đề phổ biến của sinh viên. | Medium | FR-MGT-02, WF-07 |

### 4.4. Security and Access

| ID | Product Backlog Item | Description | Expected Value | Priority | Related Requirements |
|---|---|---|---|---|---|
| PBI-12 | Role-based Access Control | Kiểm soát quyền truy cập dựa trên vai trò Student, Staff và Management; hỗ trợ Management xem thông tin người dùng và quản lý vai trò theo quyền được cấp. | Bảo đảm người dùng chỉ truy cập các chức năng và dữ liệu phù hợp với quyền hạn của mình. | High | FR-SEC-01, AC-12 |
| PBI-13 | Audit Logging & Data Access Protection | Ghi nhận các hoạt động quan trọng, người thực hiện, thời điểm và những thay đổi liên quan đến Request; hỗ trợ kiểm tra lịch sử xử lý và bảo vệ dữ liệu theo quyền truy cập. | Tăng khả năng theo dõi, kiểm tra hoạt động và bảo vệ thông tin sinh viên. | High | FR-SEC-02, AC-13 |

### 4.5. Product Backlog Notes

- PBI-01 User Authentication là chức năng hỗ trợ việc xác thực người dùng. Chi tiết về phương thức đăng nhập và cơ chế xác thực cần được đối chiếu với FR-SEC-01.
- PBI-03 Request Tracking có Priority Medium theo mức ưu tiên hiện tại của FR-STU-02. Tuy nhiên, đây vẫn là chức năng thuộc Mandatory Project Scope và phải được xem xét trong phạm vi sản phẩm.
- PBI-12 Role-based Access Control giữ nội dung kiểm soát quyền theo ba vai trò. Phần Management xem thông tin người dùng và cập nhật Role cần được xác nhận về phạm vi và Acceptance Criteria trước khi chốt triển khai.
- PBI-13 Audit Logging & Data Access Protection phải được xem xét cùng các yêu cầu về Security, Privacy và Data Protection.
- Các PBI không thay thế Functional Requirements hoặc Acceptance Criteria. Chi tiết về điều kiện thực hiện và kết quả mong đợi được mô tả trong các tài liệu tương ứng.

## 5. Feedback Management

Feedback Management là quy trình tiếp nhận, ghi nhận, phân loại và đánh giá ý kiến từ Client và Stakeholders để xác định những nội dung cần cải thiện trong UniSupport.

Quy trình này giúp bảo đảm các thay đổi đối với sản phẩm được xem xét có căn cứ và phù hợp với Project Scope.

### 5.1. Feedback Sources

Feedback có thể được thu thập từ:

- Client / Project Sponsor sau khi xem xét các phần prototype được bàn giao.
- Student Representative trong các hoạt động Usability Testing.
- Staff Representative trong quá trình đánh giá Staff Workspace.
- Management Representative trong quá trình đánh giá Dashboard và Reporting.
- Kết quả Test Scenarios và các vấn đề phát hiện trong quá trình kiểm thử.

Feedback từ Client sau mỗi milestone cần được ghi nhận để nhóm xem xét trước khi tiếp tục hoàn thiện các chức năng liên quan.

Đối với dự án hiện tại, GitHub Issues được sử dụng làm nơi ghi nhận và theo dõi Feedback. Các kênh trao đổi trực tiếp khác, nếu có, cần được tổng hợp vào GitHub để tránh thất lạc thông tin.

### 5.2. Feedback Classification

Feedback được phân loại theo nội dung và mục đích xử lý.

| Classification | Description | Expected Action |
|---|---|---|
| Bug Report | Phản ánh chức năng hoạt động không đúng với yêu cầu hoặc Expected Result đã xác định. | Ghi nhận Bug, đánh giá mức độ ảnh hưởng và tạo công việc sửa lỗi phù hợp. |
| Change Request | Đề xuất thay đổi chức năng, yêu cầu, phạm vi hoặc cách hoạt động hiện tại của sản phẩm. | Đánh giá ảnh hưởng đến Scope, Effort, Schedule và các tài liệu liên quan trước khi xem xét phê duyệt. |
| Feature Request | Đề xuất chức năng mới chưa có trong Product Backlog hiện tại. | Đánh giá mức độ phù hợp với Product Goals và Product Scope trước khi xem xét bổ sung. |
| Improvement Suggestion | Đề xuất cải thiện chức năng hoặc trải nghiệm người dùng hiện có. | Đánh giá giá trị mang lại và khả năng thực hiện. |
| General Feedback | Ý kiến chung về sản phẩm, quy trình hoặc trải nghiệm sử dụng chưa thuộc các nhóm trên. | Ghi nhận và xem xét để xác định hành động phù hợp. |

Việc phân loại giúp nhóm xác định đúng loại công việc cần xử lý. Không phải mọi Feedback đều dẫn đến việc bổ sung chức năng hoặc thay đổi Product Backlog.

### 5.3. Feedback Evaluation and Prioritization

Sau khi được ghi nhận và phân loại, Feedback được đánh giá dựa trên các yếu tố:

- Mức độ phù hợp với Project Goals và Product Scope.
- Giá trị mang lại cho Student, Staff và Management.
- Mức độ ảnh hưởng đến các chức năng hiện tại.
- Mức độ cần thiết và ảnh hưởng đến chất lượng sản phẩm.
- Effort dự kiến và khả năng thực hiện trong giới hạn nguồn lực.
- Các Dependencies với Functional Requirements, Workflows và những PBI khác.

Feedback có thể được xử lý theo các hướng:

- **Accept:** Được chấp nhận để xem xét cập nhật Product Backlog hoặc tạo công việc thực hiện.
- **Defer:** Được giữ lại để xem xét trong giai đoạn sau.
- **Reject:** Không được đưa vào phạm vi thực hiện vì không phù hợp với mục tiêu, phạm vi hoặc giới hạn dự án. Lý do cần được ghi nhận.
- **Need Clarification:** Chưa đủ thông tin để đưa ra quyết định và cần trao đổi thêm với người gửi Feedback.

Việc đánh giá Priority sử dụng các tiêu chí tại mục 3.1. Không tự động thay đổi Priority chỉ dựa trên thời điểm nhận Feedback.

### 5.4. Backlog Update Process

Quy trình xử lý Feedback và cập nhật Product Backlog:

1. **Receive Feedback:** Tiếp nhận ý kiến từ Client hoặc Stakeholders sau khi đánh giá prototype, milestone hoặc các hoạt động kiểm thử.
2. **Record Feedback:** Ghi nhận nội dung, người gửi, thời điểm và chức năng liên quan trong GitHub Issues.
3. **Classify Feedback:** Xác định Feedback thuộc Bug Report, Change Request, Feature Request, Improvement Suggestion hoặc General Feedback.
4. **Evaluate Feedback:** Đánh giá giá trị, phạm vi ảnh hưởng, Dependencies và Effort dự kiến.
5. **Prioritize:** Xác định mức độ ưu tiên dựa trên các tiêu chí Priority Evaluation.
6. **Review and Decision:** Nhóm xem xét và đề xuất hướng xử lý. Những thay đổi cần Client/Sponsor chấp thuận phải được xác nhận trước khi thực hiện.
7. **Update Product Backlog:** Cập nhật PBI, Priority, Expected Value và các liên kết tài liệu nếu Feedback được chấp nhận.
8. **Update Related Documents:** Nếu thay đổi ảnh hưởng đến yêu cầu, kế hoạch, công việc hoặc kiểm thử, các tài liệu liên quan phải được cập nhật đồng bộ.
9. **Track Implementation:** Tạo hoặc cập nhật GitHub Issues để theo dõi người phụ trách, tiến độ và kết quả thực hiện.
10. **Verify Result:** Kiểm tra kết quả sau khi thay đổi được thực hiện và ghi nhận trạng thái xử lý Feedback.

### 5.5. Feedback Approval and Ownership

Trong quá trình thực hiện dự án:

- **Project Management Team:** Tiếp nhận, ghi nhận, phân loại và đánh giá Feedback; đề xuất Priority và phạm vi thay đổi.
- **Business Analyst:** Hỗ trợ phân tích ảnh hưởng của Feedback đến Functional Requirements, Business Rules và Acceptance Criteria.
- **Project Sponsor / Client:** Xem xét và xác nhận các thay đổi ảnh hưởng đến Project Scope, mục tiêu hoặc các yêu cầu đã thống nhất.

Thẩm quyền quyết định cuối cùng đối với các thay đổi sau bàn giao và người chịu trách nhiệm quản lý Product Backlog lâu dài cần được Client xác nhận.

## 6. Value Metrics

Value Metrics được sử dụng để đánh giá mức độ UniSupport đáp ứng các mục tiêu và mang lại giá trị cho các nhóm người dùng.

Các chỉ số dưới đây được xây dựng dựa trên Required Project Outcomes trong đề bài.

| ID | Value Metric | Target | Measurement Method |
|---|---|---|---|
| VM-01 | Request Assignment Coverage | At least 90% | Tỷ lệ Request có Department hoặc Staff chịu trách nhiệm rõ ràng trên tổng số Request được ghi nhận. |
| VM-02 | Request Tracking Coverage | At least 90% | Tỷ lệ Request có Status được ghi nhận và có thể theo dõi trên tổng số Request được ghi nhận. |
| VM-03 | Student Progress Inquiry Reduction | At least 30% reduction | So sánh số lần Student phải liên hệ để hỏi tiến độ trước và sau khi sử dụng quy trình theo dõi Request. |
| VM-04 | Overdue Request Visibility | Management có thể nhận biết Request quá hạn | Kiểm tra Dashboard có hiển thị danh sách Request quá hạn và cảnh báo tương ứng. |
| VM-05 | Common Issue Identification | Management có thể xác định các vấn đề phổ biến | Kiểm tra báo cáo thống kê Request theo Request Type. |
| VM-06 | Authorized Data Access | Chỉ người có thẩm quyền được truy cập dữ liệu | Thực hiện kiểm thử quyền truy cập bằng các tài khoản Student, Staff và Management. |
| VM-07 | Student Satisfaction Monitoring | Có khả năng theo dõi Feedback và mức độ hài lòng | Kiểm tra dữ liệu Feedback được lưu và hiển thị trong báo cáo phù hợp. |

### 6.1. Measurement Approach

Việc đánh giá Value Metrics được thực hiện thông qua:

- Prototype Demonstration: Kiểm tra các chức năng chính của UniSupport.
- Test Scenarios: Xác minh các workflow và kết quả mong đợi.
- Usability Testing: Quan sát Student và Staff thực hiện các tác vụ chính.
- Simulated Data: Sử dụng dữ liệu giả lập để kiểm tra khả năng tổng hợp và hiển thị thông tin.
- Dashboard and Reporting Review: Kiểm tra các chỉ số và báo cáo dành cho Management.

Đối với các chỉ số cần so sánh trước và sau khi sử dụng hệ thống, nhóm cần có dữ liệu baseline phù hợp. Nếu chưa có dữ liệu thực tế, kết quả chỉ được ghi nhận ở mức mô phỏng và không được xem là kết quả cải thiện thực tế của Aurora University.

Các chỉ số về mức độ hài lòng được theo dõi thông qua Feedback. Hiện chưa có mục tiêu phần trăm hài lòng cụ thể được Client xác nhận.

## 7. Backlog Review and Change Management

Product Backlog cần được xem xét và cập nhật khi:

- Client cung cấp Feedback mới.
- Có thay đổi đối với Functional Requirements hoặc Product Scope.
- Phát hiện lỗi ảnh hưởng đến các chức năng chính.
- Có thay đổi về Dependencies giữa các chức năng.
- Effort hoặc nguồn lực không còn phù hợp với kế hoạch.
- Có kết quả kiểm thử hoặc đánh giá Usability cần cải thiện.

Khi có thay đổi:

1. Ghi nhận nội dung thay đổi trong GitHub Issues.
2. Đánh giá ảnh hưởng đến các PBI và tài liệu liên quan.
3. Xác định Priority và Effort dự kiến.
4. Xác định người có thẩm quyền xem xét và chấp thuận.
5. Cập nhật Product Backlog sau khi có quyết định phù hợp.
6. Cập nhật Functional Requirements, Acceptance Criteria, Test Scenarios, WBS và các tài liệu liên quan nếu cần.
7. Theo dõi việc thực hiện và xác minh kết quả.

Mọi thay đổi quan trọng cần có lý do và thông tin tham chiếu để bảo đảm khả năng truy vết.

## 8. Scope and Implementation Notes

Product Backlog hiện tại được xây dựng ở mức high-level để xác định các chức năng chính của prototype UniSupport.

Việc lựa chọn và triển khai chức năng phải tuân thủ các giới hạn sau:

- Tổng thời gian dự án là 15 tuần.
- Tổng ngân sách lao động tối đa là 320 person-hours.
- Prototype và testing sử dụng Simulated Data.
- Hệ thống xem xét ba nhóm người dùng Student, Staff và Management.
- Giải pháp xem xét khả năng sử dụng trên thiết bị di động và máy tính.
- Giải pháp xem xét hỗ trợ tiếng Việt và tiếng Anh.
- Các chức năng phải phù hợp với Mandatory Project Scope và các yêu cầu đã được xác nhận.

Các nội dung sau không thuộc phạm vi triển khai chính trong giai đoạn hiện tại:

- Production-ready System hoàn chỉnh.
- Tích hợp thực tế với toàn bộ hệ thống của trường.
- Sử dụng dữ liệu cá nhân thật.
- Thay thế hệ thống quản lý đào tạo.
- Xử lý thanh toán học phí.
- Tự động đưa ra quyết định học vụ.
- Triển khai trên quy mô toàn trường.

Những nội dung này có thể được xem xét trong Future Roadmap nếu có nhu cầu và được chấp thuận phù hợp.

Các chi tiết về giao diện, Business Rules, dữ liệu, Functional Requirements, Acceptance Criteria và Test Scenarios được mô tả trong các tài liệu liên quan.

## 9. Related Documents

| Document | Purpose |
|---|---|
| [Product Goals](./product-goals.md) | Xác định mục tiêu và kết quả mong đợi của sản phẩm. |
| [Product Scope](./product-scope.md) | Xác định phạm vi chức năng của UniSupport. |
| [Problem Statement](./problem-statement.md) | Mô tả các vấn đề của Student, Staff và Management. |
| [Users and Roles](../02-domain/users-and-roles.md) | Xác định các nhóm người dùng và trách nhiệm của từng vai trò. |
| [Module PRDs](../03-modules/README.md) | Mô tả chức năng chi tiết của từng Module. |
| [Workflows](../04-workflows/) | Mô tả quy trình nghiệp vụ của UniSupport. |
| [Functional Requirements](../05-requirements/functional-requirements.md) | Xác định các yêu cầu chức năng. |
| [Non-Functional Requirements](../05-requirements/non-functional-requirements.md) | Xác định các yêu cầu phi chức năng. |
| [Acceptance Criteria](../06-acceptance/acceptance-criteria.md) | Xác định điều kiện chấp nhận cho các yêu cầu. |
| [Test Scenarios](../06-acceptance/test-scenarios.md) | Xác định các kịch bản kiểm thử chức năng và phi chức năng. |
| [Feedback Process](../10-product-management/feedback-process.md) | Mô tả quy trình tiếp nhận, phân loại và xử lý Feedback. |
| [Success Metrics](../10-product-management/success-metrics.md) | Theo dõi các chỉ số đánh giá giá trị và kết quả sản phẩm. |
| [Product Roadmap](../10-product-management/roadmap.md) | Xác định định hướng phát triển tính năng theo các milestone. |