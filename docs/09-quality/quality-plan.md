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

Khi phát hiện lỗi hoặc vấn đề chất lượng, nhóm thực hiện các bước sau:

1. Ghi nhận lỗi và mô tả cách tái hiện lỗi.
2. Xác định chức năng hoặc deliverable bị ảnh hưởng.
3. Đánh giá mức độ ảnh hưởng và ưu tiên xử lý.
4. Giao lỗi cho thành viên phụ trách.
5. Kiểm tra lại sau khi sửa lỗi.
6. Cập nhật trạng thái lỗi và lưu kết quả kiểm tra.

Nhóm sử dụng các mức độ ưu tiên sau:

| Priority | Description |
|---|---|
| High | Lỗi ảnh hưởng đến chức năng chính, workflow quan trọng hoặc quyền truy cập dữ liệu. |
| Medium | Lỗi ảnh hưởng đến một phần chức năng hoặc gây khó khăn đáng kể cho người dùng. |
| Low | Lỗi giao diện, nội dung hoặc vấn đề nhỏ không ảnh hưởng đáng kể đến workflow chính. |

## 7. Deliverable Acceptance

Một deliverable được xem xét để nghiệm thu khi:

- Nội dung đáp ứng scope và requirements đã thống nhất.
- Các tiêu chí chất lượng liên quan đã được kiểm tra.
- Những lỗi nghiêm trọng ảnh hưởng đến mục đích sử dụng đã được xử lý.
- Kết quả review và testing được ghi nhận.
- Tài liệu liên quan được cập nhật nếu có thay đổi.

Client hoặc Project Sponsor sẽ xem xét và chấp nhận deliverables theo các Acceptance Criteria được thống nhất. Nếu deliverable chưa đạt yêu cầu, nhóm cần ghi nhận phản hồi và thực hiện điều chỉnh phù hợp.

## 8. Quality Responsibilities

| Role | Quality Responsibilities |
|---|---|
| Project Manager | Theo dõi hoạt động chất lượng, điều phối review và theo dõi các vấn đề chưa được xử lý. |
| Business Analyst | Kiểm tra requirements, workflow và các tiêu chí nghiệm thu nghiệp vụ. |
| Front-end Developer | Kiểm tra giao diện, khả năng responsive và các chức năng phía người dùng. |
| Back-end Developer | Kiểm tra logic xử lý, dữ liệu và cơ chế phân quyền. |

## 9. Quality Records

Nhóm cần lưu lại các thông tin sau trong quá trình kiểm soát chất lượng:

- Requirements Review Results.
- Design Review Feedback.
- Test Scenarios and Test Results.
- Defect Records.
- Usability Testing Feedback.
- Deliverable Review and Acceptance Records.

Các kết quả này được sử dụng để theo dõi chất lượng, xác định vấn đề cần cải thiện và hỗ trợ Project Handover.