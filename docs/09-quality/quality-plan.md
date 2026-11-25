# Quality Plan

## 1. Purpose

Tài liệu này xác định cách nhóm quản lý và kiểm soát chất lượng trong quá trình thực hiện dự án UniSupport. Mục tiêu là bảo đảm các deliverables đáp ứng yêu cầu đã thống nhất, có thể kiểm tra được và phù hợp với phạm vi dự án.

## 2. Quality Objectives

Nhóm tập trung vào các mục tiêu chất lượng sau:

- Đảm bảo các chức năng chính đáp ứng Mandatory Project Scope.
- Đảm bảo prototype có thể minh họa các workflow chính của sinh viên, nhân viên và ban quản lý.
- Đảm bảo giao diện có thể sử dụng trên thiết bị di động và máy tính.
- Xem xét khả năng hỗ trợ tiếng Việt và tiếng Anh.
- Đảm bảo dữ liệu giả lập được sử dụng trong prototype và testing.
- Kiểm tra các yêu cầu về Security & Privacy, bao gồm xác thực và phân quyền theo vai trò.
- Đảm bảo tài liệu dự án đầy đủ và đủ rõ ràng để nhóm khác có thể tiếp nhận.

## 3. Quality Assurance Activities

Nhóm thực hiện các hoạt động nhằm phòng ngừa lỗi và duy trì chất lượng trong quá trình phát triển.

| Activity | Description | Responsible |
|---|---|---|
| Requirements Review | Kiểm tra requirements để bảo đảm nội dung rõ ràng, nhất quán và phù hợp với Project Scope. | Project Manager / Business Analyst |
| Design Review | Rà soát workflow, wireframe và UI/UX trước khi hoàn thiện prototype. | Business Analyst / Front-end Developer |
| Development Review | Kiểm tra source code và các chức năng được phát triển trước khi tích hợp. | Front-end Developer / Back-end Developer |
| Documentation Review | Kiểm tra tính đầy đủ và nhất quán của các tài liệu dự án. | Project Manager / Business Analyst |
| Stakeholder Review | Thu thập phản hồi tại các buổi review và xem xét các điểm cần cải thiện. | Project Manager |

## 4. Quality Control and Testing

Nhóm thực hiện kiểm tra prototype và các deliverables để phát hiện lỗi, thiếu sót hoặc nội dung chưa đáp ứng yêu cầu.

| Testing Type | Description |
|---|---|
| Functional Testing | Kiểm tra các chức năng gửi, phân loại, phân công, xử lý và theo dõi yêu cầu. |
| Workflow Testing | Kiểm tra luồng xử lý từ lúc sinh viên gửi yêu cầu đến khi nhân viên hoàn tất và đóng yêu cầu. |
| Role-based Access Testing | Kiểm tra quyền truy cập tương ứng với vai trò sinh viên, nhân viên và quản lý. |
| Responsive Testing | Kiểm tra giao diện trên thiết bị di động và máy tính. |
| Usability Testing | Thu thập phản hồi từ đại diện sinh viên và nhân viên về mức độ dễ sử dụng của prototype. |
| Data and Reporting Testing | Sử dụng dữ liệu giả lập để kiểm tra việc phân công, theo dõi số lượng yêu cầu, yêu cầu quá hạn và báo cáo. |
| Documentation Review | Kiểm tra các tài liệu bàn giao để bảo đảm nhóm khác có thể hiểu và tiếp tục công việc. |

## 5. Quality Criteria

Các tiêu chí dưới đây được sử dụng làm cơ sở đánh giá chất lượng của dự án.

| ID | Quality Criteria | Verification Method |
|---|---|---|
| QC-01 | Các chức năng chính phải đáp ứng Mandatory Project Scope. | Functional Testing |
| QC-02 | Ít nhất 90% yêu cầu trong kịch bản kiểm thử phải có người chịu trách nhiệm rõ ràng. | Scenario Testing |
| QC-03 | Ít nhất 90% yêu cầu trong kịch bản kiểm thử phải có trạng thái có thể theo dõi. | Scenario Testing |
| QC-04 | Ban quản lý có thể nhận biết các yêu cầu quá hạn và các loại vấn đề phổ biến. | Data and Reporting Testing |
| QC-05 | Quyền truy cập dữ liệu phải phù hợp với vai trò người dùng. | Role-based Access Testing |
| QC-06 | Prototype phải được kiểm tra trên thiết bị di động và máy tính. | Responsive Testing |
| QC-07 | Prototype phải xem xét khả năng sử dụng tiếng Việt và tiếng Anh. | UI Review |
| QC-08 | Prototype và testing phải sử dụng dữ liệu giả lập. | Data Review |
| QC-09 | Các tài liệu bàn giao phải đầy đủ và dễ hiểu đối với nhóm tiếp nhận. | Documentation Review |

Lưu ý: Các mục tiêu giảm yêu cầu bị bỏ sót, xử lý trùng lặp và giảm ít nhất 30% số lần sinh viên liên hệ hỏi tiến độ sẽ được đánh giá thông qua test scenarios, usability testing hoặc dữ liệu giả lập phù hợp. Kết quả kiểm thử prototype không được xem là bằng chứng rằng hiệu quả vận hành thực tế của trường đã được cải thiện.

## 6. Defect Management

### 6.1 Shared Severity Scale

Severity là thang đo chung cho các lỗi và khiếm khuyết trong Quality Plan, Project Governance, Feedback Process và mẫu báo cáo lỗi trên GitHub. Mức độ nghiêm trọng mô tả tác động; Thứ tự ưu tiên/thứ tự công việc tồn đọng của sản phẩm là một quyết định lập kế hoạch riêng biệt.

| Severity | Definition | Initial response target (team planning target) | Resolution / disposition target | Milestone release impact |
|---|---|---|---|---|
| Critical | Prototype không thể sử dụng cho quy trình công việc cốt lõi; xảy ra tình trạng mất/hỏng dữ liệu; hoặc xác nhận có nguy cơ truy cập trái phép nghiêm trọng. | Phân loại ngay lập tức; thông báo cho Quản lý sản phẩm (PM) ngay lập tức. | Khắc phục hoặc vô hiệu hóa quy trình bị ảnh hưởng và kiểm chứng trước khi quyết định phát hành; không được phép tồn tại lỗi Nghiêm trọng chưa xử lý khi phát hành. | Ngăn chặn việc phát hành. |
| High | Một quy trình/yêu cầu bắt buộc bị lỗi, hoặc tồn tại vấn đề nghiêm trọng về quyền truy cập/dữ liệu mà không có giải pháp thay thế chấp nhận được. | Phân loại trong vòng 1 ngày làm việc; thông báo cho PM và lập trình viên liên quan. | Lên kế hoạch khắc phục và kiểm chứng trong vòng 3 ngày làm việc, hoặc lập tài liệu về việc leo thang vấn đề và quyết định ngăn chặn phát hành. | Ngăn chặn việc phát hành nếu chưa được xử lý. |
| Medium | Chức năng bị ảnh hưởng một phần, nhưng vẫn có giải pháp thay thế hợp lý và không có vấn đề nghiêm trọng về bảo mật/dữ liệu. | Phân loại trong vòng 2 ngày làm việc. | Lên kế hoạch giải quyết hoặc đưa ra phương án xử lý trong vòng 5 ngày làm việc. | Có thể tồn tại nếu có giải pháp thay thế, xác định được người chịu trách nhiệm, ngày dự kiến ​​hoàn thành và chấp nhận các vấn đề còn tồn đọng; không được phép có quá 3 lỗi mức Trung bình chưa xử lý khi phát hành. |
| Low | Các vấn đề về giao diện, cách dùng từ, khả năng sử dụng nhỏ hoặc các vấn đề không thuộc chức năng cốt lõi với tác động hạn chế. | Phân loại trong vòng 3 ngày làm việc. | Lên kế hoạch giải quyết hoặc đưa ra phương án xử lý trong vòng 10 ngày làm việc. | Có thể tồn tại nếu đã xác định được người chịu trách nhiệm và ngày dự kiến ​​hoàn thành; không tự thân gây ngăn chặn việc phát hành. |

Đây là các mục tiêu lập kế hoạch nội bộ, không phải là thỏa thuận mức dịch vụ (SLA) vận hành đã cam kết với Đại học Aurora. Các mục tiêu có thể được đánh giá lại nếu các yếu tố phụ thuộc hoặc nỗ lực bị ảnh hưởng; người quản lý dự án sẽ ghi lại quyết định và việc báo cáo lên cấp trên.

### 6.2 Defect Workflow

Khi phát hiện lỗi hoặc vấn đề chất lượng, nhóm thực hiện các bước sau:

1. Ghi nhận lỗi và mô tả cách tái hiện lỗi.
2. Xác định chức năng hoặc deliverable bị ảnh hưởng.
3. Đánh giá mức độ ảnh hưởng và ưu tiên xử lý.
4. Giao lỗi cho thành viên phụ trách.
5. Kiểm tra lại sau khi sửa lỗi.
6. Cập nhật trạng thái lỗi và lưu kết quả kiểm tra.

Mỗi Bug record cần ghi Severity, steps to reproduce, expected/actual result, affected requirement/test scenario, assignee, date reported, target date, status và verification evidence. PM/BA xác nhận Severity ban đầu; người sửa không tự hạ mức mà không ghi lý do và review.

## 7. Release Gate and Deliverable Acceptance

### 7.1 Milestone Release Gate

Một milestone chỉ được đề xuất release/acceptance khi tất cả điều kiện sau được kiểm tra và ghi evidence:

- 0 open Critical defects.
- 0 open High defects.
- Không quá 3 open Medium defects; từng lỗi phải có workaround, owner, target date, residual-risk note và quyết định chấp nhận được ghi lại.
- Open Low defects phải có owner và target date; được liệt kê trong release notes/known issues.
- 100% Test Scenarios đánh dấu Critical/Core workflow cho milestone đã thực thi; tất cả đều Pass hoặc có defect record và release-blocking decision tương ứng.
- Regression scenarios của các workflow đã bàn giao ở milestone trước được thực thi; các scenario trọng yếu đều Pass.
- QC-xx liên quan milestone có evidence; không chỉ ghi “reviewed”.
- Deliverables, test evidence, known issues và decision record được cập nhật.

PM tổng hợp evidence; BA kiểm tra acceptance criteria và test evidence; FE/BE xác nhận defect fixes; Project Sponsor / Simulated Client quyết định acceptance theo Governance. Nếu gate không đạt, PM đề xuất lùi release hoặc xin quyết định có ghi nhận rủi ro; không tự coi milestone đã đạt.

### 7.2 QC Verification Clarifications

| QC ID | Verification clarification |
|---|---|
| QC-01 | Trace từng Mandatory Scope item đến FR/AC/TS; thực thi các scenario liên quan và ghi Pass/Fail/evidence. |
| QC-02 | Tính tỷ lệ Request trong dataset/scenario có owner rõ ràng; target ≥90%. |
| QC-03 | Tính tỷ lệ Request trong dataset/scenario có status trackable; target ≥90%. |
| QC-04 | Dùng dataset có overdue và Request Type; xác minh Dashboard hiển thị overdue và tổng hợp type đối chiếu dữ liệu nguồn. |
| QC-05 | Chạy Role Permission Test Scenarios; tất cả test access boundary phải Pass, unauthorized access phải bị từ chối. |
| QC-06 | Thực thi các scenario đã chọn trên mobile-size và desktop-size; ghi viewport và evidence. |
| QC-07 | Kiểm tra danh sách UI text/key chính trong cả tiếng Việt và tiếng Anh; ghi missing/incorrect text; không chỉ ghi “considered”. |
| QC-08 | Kiểm tra dataset, attachment và test records; xác nhận không dùng dữ liệu cá nhân thật. |
| QC-09 | Dùng handover checklist: tài liệu có link, phiên bản, hướng dẫn, known issues và người tiếp nhận có thể lần theo workflow. |

## 8. Deliverable Acceptance

Một deliverable được xem xét để nghiệm thu khi:

- Nội dung đáp ứng scope và requirements đã thống nhất.
- Các tiêu chí chất lượng liên quan đã được kiểm tra.
- Những lỗi nghiêm trọng ảnh hưởng đến mục đích sử dụng đã được xử lý.
- Kết quả review và testing được ghi nhận.
- Tài liệu liên quan được cập nhật nếu có thay đổi.

Client hoặc Project Sponsor sẽ xem xét và chấp nhận deliverables theo các Acceptance Criteria được thống nhất. Nếu deliverable chưa đạt yêu cầu, nhóm cần ghi nhận phản hồi và thực hiện điều chỉnh phù hợp.

## 9. Quality Responsibilities

| Role | Quality Responsibilities |
|---|---|
| Project Manager | Theo dõi hoạt động chất lượng, điều phối review và theo dõi các vấn đề chưa được xử lý. |
| Business Analyst | Kiểm tra requirements, workflow và các tiêu chí nghiệm thu nghiệp vụ. |
| Front-end Developer | Kiểm tra giao diện, khả năng responsive và các chức năng phía người dùng. |
| Back-end Developer | Kiểm tra logic xử lý, dữ liệu và cơ chế phân quyền. |

## 10. Quality Records

Nhóm cần lưu lại các thông tin sau trong quá trình kiểm soát chất lượng:

- Requirements Review Results.
- Design Review Feedback.
- Test Scenarios and Test Results.
- Defect Records.
- Usability Testing Feedback.
- Deliverable Review and Acceptance Records.

Các kết quả này được sử dụng để theo dõi chất lượng, xác định vấn đề cần cải thiện và hỗ trợ Project Handover.