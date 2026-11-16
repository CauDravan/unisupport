# Data Requirements

## 1. Purpose

Tài liệu mô tả các nhóm dữ liệu UniSupport cần quản lý, mục đích sử dụng, quan hệ với chức năng nghiệp vụ và các yêu cầu bảo vệ dữ liệu. Tài liệu tập trung vào **loại dữ liệu và cách sử dụng ở mức nghiệp vụ**; thuộc tính chi tiết của Request nằm trong [Request Model](../02-domain/request-model.md), còn quan hệ dữ liệu được mô tả trong [ERD](./erd.md).

## 2. User and Role Data

Dữ liệu User xác định người sử dụng UniSupport và hỗ trợ xác thực, phân quyền, liên kết hoạt động với người thực hiện.

Các nhóm người dùng:
- **Student:** gửi và theo dõi Request của mình, cung cấp thông tin bổ sung và gửi Feedback.
- **Staff:** tiếp nhận, phân loại, phân công và xử lý Request trong phạm vi quyền được cấp.
- **Management:** theo dõi hoạt động và xem Dashboard/báo cáo theo quyền được cấp.

Role được mô tả ở mức ba nhóm Student, Staff và Management. Hệ thống sử dụng Role đã được gán cho User để xác định và áp dụng quyền truy cập. Chức năng Management trực tiếp xem danh sách User và cập nhật Role (Role Administration) không thuộc phạm vi bàn giao hiện tại; có thể được xem xét trong Future Enhancement nếu được Project Sponsor phê duyệt.

## 3. Department and Request Type Data

- **Department Data:** xác định bộ phận chịu trách nhiệm xử lý Request. Dữ liệu này được sử dụng trong Classification, Assignment, Transfer và báo cáo workload theo Department.
- **Request Type Data:** danh mục loại yêu cầu được hệ thống hỗ trợ. Student lựa chọn Request Type khi gửi; Staff có thể phân loại Request; Management sử dụng dữ liệu này để thống kê các vấn đề phổ biến.

Danh sách Department, Request Type, thuộc tính chi tiết và người có quyền quản lý danh mục chưa được xác định trong nguồn; cần nhóm xác nhận bộ dữ liệu giả lập và phạm vi quản lý danh mục.

## 4. Request Data

Request Data là nhóm dữ liệu trung tâm, lưu một yêu cầu hỗ trợ từ khi được gửi đến khi giải quyết và đóng.

Theo [Request Model](../02-domain/request-model.md), Request gồm các thông tin:

- Request ID, Student ID, Request Type, Subject và Description.
- Attachments (nếu có).
- Priority, Department và Assigned Staff; Department/Assigned Staff có thể chưa xác định tại thời điểm tạo hoặc chờ phân công.
- Status, Created Date, Updated Date và Due Date.
- Resolution và Closed Date.

Request Data hỗ trợ WF-01 đến WF-06 và cung cấp dữ liệu đầu vào cho Request Tracking, Monitoring và Reporting.

## 5. Request History and Activity Data

Request History / Activity Data ghi nhận các thay đổi và hoạt động quan trọng trong vòng đời Request, bao gồm:

- Thay đổi Status, Priority, Department hoặc Assigned Staff.
- Cập nhật nội dung/hoạt động xử lý.
- Yêu cầu Student bổ sung thông tin và thông tin Student cung cấp.
- Transfer giữa Staff hoặc Department, gồm lý do chuyển.
- Ghi nhận Resolution và đóng Request.

Mỗi bản ghi lịch sử cần thể hiện người thực hiện, loại hoạt động, nội dung thay đổi và thời điểm thực hiện. Dữ liệu này hỗ trợ Staff theo dõi tiến trình và Management giám sát hoạt động.

## 6. Attachment Data

Attachment Data quản lý tài liệu/hình ảnh Student gửi kèm Request hoặc gửi bổ sung trong WF-04. Mỗi Attachment phải được liên kết với Request tương ứng và chỉ được truy cập bởi người có quyền phù hợp.

Nguồn chưa xác định metadata bắt buộc, giới hạn định dạng/kích thước, vị trí lưu nội dung tệp hoặc cơ chế quét tệp. Các chi tiết này là TBD; không mặc định sử dụng dịch vụ lưu trữ bên ngoài.

## 7. Feedback Data

Feedback Data lưu phản hồi của Student sau khi Request đã được xử lý và chuyển sang Closed.

Dữ liệu được nêu trong WF-07 và M03 PRD gồm:
- Rating.
- Comment (không bắt buộc).
- Liên kết đến Request tương ứng và Student gửi Feedback.

Feedback hỗ trợ Management theo dõi mức độ hài lòng và đánh giá chất lượng dịch vụ. Quy tắc số lượng Feedback trên mỗi Request và việc chỉnh sửa Feedback sau khi gửi chưa được xác định.

## 8. Audit Log Data

Audit Log phục vụ kiểm tra các hoạt động quan trọng và thay đổi dữ liệu theo FR-SEC-02. Thông tin tối thiểu được yêu cầu gồm:

- Actor – người thực hiện.
- Action – thao tác được thực hiện.
- Timestamp – thời điểm thực hiện.
- Đối tượng dữ liệu và thông tin/giá trị thay đổi liên quan.

Các sự kiện được nêu rõ gồm thay đổi Status, Priority, Assignment và thông tin xử lý. Đề bài còn yêu cầu xem xét lịch sử truy cập và thay đổi; danh sách event audit đầy đủ cần được nhóm xác nhận.

**Phân biệt:** Request History / Activity tập trung vào tiến trình của từng Request; Audit Log phục vụ kiểm tra hoạt động và thay đổi dữ liệu. Hai nhóm có thể tham chiếu cùng một hành động nhưng không được mặc định đồng nhất về mục đích hoặc cách lưu trữ.

## 9. Notification Data

Các yêu cầu nghiệp vụ yêu cầu Student được thông báo khi Status thay đổi hoặc khi Staff yêu cầu bổ sung thông tin. Tuy nhiên, tài liệu nguồn chưa xác định Notification có được lưu thành dữ liệu riêng hay không, cũng chưa quy định kênh gửi, trạng thái gửi, retry hoặc lịch sử thông báo.

Vì vậy, Notification được ghi nhận là **data/design item cần xác nhận**, không tự thêm một entity hoặc tích hợp dịch vụ thông báo vào phạm vi kiến trúc hiện tại.

## 10. Data Usage and Traceability

| Data Group | Main Usage | Related Requirements / Workflows |
|---|---|---|
| User and Role Data | Xác định người dùng, Role và phạm vi truy cập. | FR-SEC-01; M04; áp dụng xuyên suốt M01–M03. |
| Department Data | Assignment, Transfer và tổng hợp workload. | FR-STA-01, FR-STA-03, FR-MGT-02; WF-02, WF-05. |
| Request Type Data | Student chọn loại, Staff phân loại, Management thống kê. | FR-STU-01, FR-STA-01, FR-MGT-02; WF-01, WF-02. |
| Request Data | Tạo, phân công, xử lý, theo dõi và báo cáo Request. | FR-STU-01/02, FR-STA-01/02/03, FR-MGT-01/02; WF-01–WF-06. |
| Request History / Activity Data | Theo dõi thay đổi và hoạt động xử lý. | FR-STA-03, FR-SEC-02; WF-02–WF-06. |
| Attachment Data | Lưu/liên kết tài liệu hỗ trợ với Request. | FR-STU-01, FR-STA-03; WF-01, WF-03, WF-04. |
| Feedback Data | Ghi nhận Rating/Comment và đánh giá dịch vụ. | FR-STU-03, FR-MGT-02; WF-07. |
| Audit Log Data | Kiểm tra actor, action, thời điểm và đối tượng thay đổi. | FR-SEC-02; NFR-SEC-05; NFR-REL-02. |
| Notification Data | Hỗ trợ thông báo Status change và yêu cầu bổ sung. | FR-STU-02/03; WF-04, WF-06. Cấu trúc dữ liệu TBD. |

## 11. Data Privacy and Integrity

- Prototype và testing chỉ sử dụng dữ liệu giả lập; không nạp dữ liệu cá nhân thật của sinh viên.
- Student chỉ truy cập Request và Attachment thuộc tài khoản của mình.
- Staff chỉ truy cập Request thuộc Department/phạm vi được phân công hoặc quyền được cấp.
- Management chỉ truy cập Dashboard, báo cáo và dữ liệu quản lý theo quyền được cấp.
- Transfer phải bảo toàn Request ID, nội dung, Attachment và lịch sử xử lý trước Transfer; Assignment mới phải được ghi nhận.
- Thay đổi Status, Priority, Assignment và hoạt động xử lý phải được ghi nhận nhất quán; không ghi lịch sử cho thay đổi chưa lưu thành công.
- Request phải tuân thủ Status Flow trong `request-status.md`; Feedback phải liên kết đúng Request và chỉ được gửi sau khi Request Closed.
- Thời hạn lưu trữ, archive/deletion và cách xử lý dữ liệu nhạy cảm phải tuân theo chính sách được Aurora University phê duyệt. Chính sách cụ thể hiện chưa có trong nguồn.

## 12. Open Data Decisions

| ID | Nội dung cần xác nhận | Tài liệu liên quan |
|---|---|---|
| DR-OD-01 | Thuộc tính hồ sơ User tối thiểu và cách tạo/cấp tài khoản. | Users and Roles; FR-SEC-01. |
| DR-OD-02 | User có thể có nhiều Role hay chỉ một Role? Staff thuộc một hay nhiều Department? | Users and Roles; M04 PRD; FR-SEC-01. |
| DR-OD-03 | Danh mục Department và Request Type, ai được quyền quản lý danh mục. | Request Model; WF-01, WF-02; M02 PRD. |
| DR-OD-04 | Request có thể chờ Department nhưng chưa có Assigned Staff trong bao lâu/quy tắc nào? | Request Model; WF-02; FR-STA-01. |
| DR-OD-05 | Cách lưu lịch sử Assignment/Transfer và quan hệ giữa Request History với Audit Log. | Request Model; Business Rules; FR-SEC-02; WF-05. |
| DR-OD-06 | Attachment metadata, giới hạn tệp, nơi lưu nội dung và biện pháp bảo vệ. | Request Model; NFR-SEC; M01/M02 PRD. |
| DR-OD-07 | Số lượng Feedback tối đa trên một Request và có cho phép cập nhật sau khi gửi không. | WF-07; M01/M03 PRD. |
| DR-OD-08 | Notification có cần lưu thành entity riêng, kênh gửi và trạng thái gửi. | FR-STU-02; WF-04, WF-06. |
| DR-OD-09 | Cấu hình thời gian xử lý mục tiêu/Due Date và quy tắc tính overdue. | Request Model; FR-MGT-01; M03 PRD. |
| DR-OD-10 | Thời hạn lưu trữ, archive/deletion và phân loại dữ liệu nhạy cảm. | NFR-SEC-06; Project Scope. |
| DR-OD-11 | Cách thức khởi tạo User và gán Role trước khi người dùng truy cập hệ thống; quy trình cấp tài khoản cụ thể chưa được đặc tả. | FR-SEC-01; Users and Roles; M04 PRD. |
| DR-OD-12 | Quy tắc lưu Request ở Department khi chưa xác định Assigned Staff; điều kiện được xem là đã phân công hoàn tất. | WF-02 và FR-STA-01 đang mô tả chưa thống nhất. |
| DR-OD-13 | Workflow chịu trách nhiệm chuyển Request sang Resolved và ghi nhận sự kiện tương ứng. | WF-03 và WF-06 đang có bước Resolved trùng nhau. |

## 13. Related Documents

- [Domain Overview](../02-domain/domain-overview.md)
- [Request Model](../02-domain/request-model.md)
- [Request Status](../02-domain/request-status.md)
- [Users and Roles](../02-domain/users-and-roles.md)
- [Business Rules](../02-domain/business-rules.md)
- [Functional Requirements](../05-requirements/functional-requirements.md)
- [Non-Functional Requirements](../05-requirements/non-functional-requirements.md)
- [System Context](./system-context.md)
- [Architecture Overview](./architecture-overview.md)
- [ERD](./erd.md)
