# Functional Requirements

Tài liệu này mô tả các yêu cầu chức năng (Functional Requirements) mà hệ thống UniSupport cần cung cấp cho từng nhóm người dùng. Mỗi yêu cầu xác định chức năng, điều kiện thực hiện, quy tắc nghiệp vụ và tiêu chí nghiệm thu để làm cơ sở cho thiết kế, phát triển, kiểm thử và bàn giao hệ thống.

Các yêu cầu được phân nhóm theo bốn module chính:

- M01 – Student Portal
- M02 – Staff Workspace
- M03 – Management Dashboard
- M04 – Security and Access

## 1. Student Portal

### FR-STU-01 – Request Submission

**Description**

Sinh viên có thể gửi yêu cầu hỗ trợ thông qua hệ thống bằng cách lựa chọn loại yêu cầu, cung cấp thông tin cần thiết và đính kèm tài liệu liên quan nếu cần.

**Actor**

- Primary Actor: Student

**Priority**

- High – Đây là chức năng cốt lõi để tiếp nhận yêu cầu hỗ trợ từ sinh viên.

**Preconditions**

- Student đã đăng nhập vào hệ thống.
- Danh sách Request Type có sẵn trên hệ thống.
- Student có quyền sử dụng chức năng gửi yêu cầu.

**Main Flow**

1. Student truy cập chức năng Submit Request.
2. Hệ thống hiển thị biểu mẫu gửi yêu cầu.
3. Student lựa chọn Request Type.
4. Student nhập các thông tin cần thiết và nội dung yêu cầu.
5. Student đính kèm tài liệu liên quan nếu cần.
6. Student gửi Request.
7. Hệ thống kiểm tra tính hợp lệ và đầy đủ của thông tin.
8. Hệ thống tạo Request và sinh Request ID duy nhất.
9. Hệ thống thông báo yêu cầu đã được tiếp nhận thành công.

**Business Rules**

- BR-01: Các trường thông tin bắt buộc phải được cung cấp trước khi tạo Request.
- BR-02: Request Type phải thuộc danh sách loại yêu cầu được hệ thống hỗ trợ.
- BR-03: Mỗi Request được tạo thành công phải có một Request ID duy nhất.
- BR-04: Tệp đính kèm phải đáp ứng các quy định về định dạng và dung lượng do hệ thống cấu hình.

**Alternative and Error Flows**

- AF-01: Student không cần đính kèm tài liệu nếu yêu cầu không cần tài liệu bổ sung.
- EF-01: Nếu thiếu thông tin bắt buộc, hệ thống thông báo các trường cần bổ sung và không tạo Request.
- EF-02: Nếu Request Type không hợp lệ, hệ thống yêu cầu Student lựa chọn lại.
- EF-03: Nếu tệp đính kèm không đáp ứng quy định, hệ thống thông báo lỗi và yêu cầu Student thay thế tệp.

**Acceptance Criteria**

- FR-STU-01/AC-01: Hệ thống hiển thị biểu mẫu cho phép Student nhập thông tin và lựa chọn Request Type.
- FR-STU-01/AC-02: Hệ thống không tạo Request khi thiếu bất kỳ trường thông tin bắt buộc nào.
- FR-STU-01/AC-03: Hệ thống tạo Request ID duy nhất sau khi Request được gửi thành công.
- FR-STU-01/AC-04: Hệ thống cho phép gửi Request không có tệp đính kèm khi tài liệu không bắt buộc.
- FR-STU-01/AC-05: Hệ thống từ chối tệp đính kèm không đáp ứng quy định được cấu hình.
- FR-STU-01/AC-06: Student nhận được thông báo xác nhận sau khi Request được tiếp nhận thành công.

**Edge Cases**

- Student gửi biểu mẫu chỉ chứa khoảng trắng trong trường nội dung bắt buộc.
- Student gửi nhiều Request có nội dung giống nhau.
- Student tải lên tệp có định dạng không được hỗ trợ.
- Student gửi biểu mẫu khi phiên đăng nhập đã hết hạn.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- Workflow: [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)

---

### FR-STU-02 – Request Tracking and Notifications

**Description**

Sinh viên có thể theo dõi trạng thái hiện tại, lịch sử cập nhật và nhận thông báo liên quan đến các Request đã gửi.

**Actor**

- Primary Actor: Student
- Supporting Actor: Staff

**Priority**

- Medium – Giúp sinh viên chủ động theo dõi tiến độ và hạn chế việc liên hệ nhiều lần để hỏi tình trạng xử lý.

**Preconditions**

- Student đã đăng nhập vào hệ thống.
- Student có ít nhất một Request đã được tạo thành công.

**Main Flow**

1. Student truy cập chức năng Request Tracking.
2. Hệ thống hiển thị danh sách Request thuộc tài khoản của Student.
3. Student lựa chọn một Request cần theo dõi.
4. Hệ thống hiển thị Request ID, Status và thông tin liên quan.
5. Hệ thống hiển thị lịch sử cập nhật phù hợp.
6. Khi Status thay đổi, hệ thống ghi nhận cập nhật và tạo thông báo cho Student.
7. Student xem thông báo và tiếp tục theo dõi Request.

**Business Rules**

- BR-01: Student chỉ được xem Request thuộc tài khoản của mình.
- BR-02: Mỗi Request phải có Status phản ánh tình trạng xử lý hiện tại.
- BR-03: Các thay đổi Status phải được ghi nhận trong lịch sử xử lý.
- BR-04: Student phải được thông báo khi có thay đổi Status hoặc khi cần bổ sung thông tin.

**Alternative and Error Flows**

- AF-01: Student có thể tìm kiếm Request bằng Request ID nếu hệ thống hỗ trợ chức năng tìm kiếm.
- EF-01: Nếu Request không tồn tại hoặc không thuộc tài khoản của Student, hệ thống không hiển thị dữ liệu Request.
- EF-02: Nếu không có lịch sử cập nhật, hệ thống hiển thị thông tin phù hợp thay vì một trang trống không có giải thích.
- EF-03: Nếu không thể tải thông tin Request, hệ thống thông báo lỗi và cho phép Student thử lại.

**Acceptance Criteria**

- FR-STU-02/AC-01: Student có thể xem danh sách Request thuộc tài khoản của mình.
- FR-STU-02/AC-02: Hệ thống hiển thị Status hiện tại của từng Request.
- FR-STU-02/AC-03: Hệ thống hiển thị lịch sử cập nhật liên quan đến Request.
- FR-STU-02/AC-04: Hệ thống tạo thông báo khi Status của Request thay đổi.
- FR-STU-02/AC-05: Hệ thống gửi thông báo cho Student khi Request chuyển sang trạng thái "Chờ bổ sung thông tin" theo yêu cầu của Staff.
- FR-STU-02/AC-06: Student không thể truy cập Request thuộc tài khoản của người dùng khác.

**Edge Cases**

- Request vừa được tạo và chưa có lịch sử cập nhật.
- Request được cập nhật nhiều lần trong thời gian ngắn.
- Student truy cập Request bằng một đường dẫn không thuộc quyền của mình.
- Request đã đóng nhưng Student vẫn truy cập lịch sử xử lý.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- Workflow: [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)
- Workflow: [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)

---

### FR-STU-03 – Additional Information and Feedback

**Description**

Sinh viên có thể cung cấp thông tin bổ sung khi Staff yêu cầu và gửi Feedback sau khi Request được giải quyết.

**Actor**

- Primary Actor: Student
- Supporting Actor: Staff

**Priority**

- Medium – Đảm bảo quá trình xử lý có đủ thông tin và cho phép sinh viên phản hồi kết quả hỗ trợ.

**Preconditions**

- Student đã đăng nhập.
- Request đã tồn tại trong hệ thống.
- Request đang ở trạng thái phù hợp với thao tác bổ sung thông tin hoặc gửi Feedback.

**Main Flow**

1. Student truy cập Request cần bổ sung thông tin hoặc gửi Feedback.
2. Hệ thống hiển thị nội dung yêu cầu bổ sung hoặc thông tin về kết quả xử lý.
3. Student cung cấp thông tin bổ sung hoặc nhập Feedback.
4. Student gửi nội dung.
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu.
6. Hệ thống lưu thông tin vào Request tương ứng.
7. Hệ thống ghi nhận hoạt động và thông báo kết quả gửi thành công.

**Business Rules**

- BR-01: Student chỉ được bổ sung thông tin cho Request thuộc tài khoản của mình.
- BR-02: Thông tin bổ sung phải được liên kết với Request tương ứng.
- BR-03: Feedback chỉ được gửi sau khi Request đã được giải quyết theo quy trình.
- BR-04: Nội dung bổ sung và Feedback phải được lưu lại để phục vụ việc theo dõi.

**Alternative and Error Flows**

- AF-01: Student có thể gửi thông tin bổ sung dưới dạng nội dung văn bản hoặc tài liệu đính kèm nếu được hỗ trợ.
- AF-02: Student có thể bỏ qua Feedback nếu không muốn gửi phản hồi.
- EF-01: Nếu Request không ở trạng thái cho phép bổ sung thông tin, hệ thống không tiếp nhận thao tác.
- EF-02: Nếu nội dung bắt buộc bị thiếu, hệ thống yêu cầu Student bổ sung trước khi gửi.
- EF-03: Nếu Request không thuộc tài khoản của Student, hệ thống từ chối truy cập.

**Acceptance Criteria**

- FR-STU-03/AC-01: Student có thể cung cấp thông tin bổ sung khi Request được yêu cầu bổ sung thông tin.
- FR-STU-03/AC-02: Hệ thống lưu thông tin bổ sung vào đúng Request.
- FR-STU-03/AC-03: Student có thể gửi Feedback sau khi Request được giải quyết.
- FR-STU-03/AC-04: Hệ thống không cho phép gửi Feedback khi Request chưa đạt điều kiện theo quy trình.
- FR-STU-03/AC-05: Hệ thống ghi nhận nội dung và thời điểm gửi Feedback.
- FR-STU-03/AC-06: Hệ thống từ chối thao tác trên Request không thuộc tài khoản của Student.

**Edge Cases**

- Student gửi thông tin bổ sung nhiều lần.
- Student gửi Feedback có nội dung trống.
- Request được đóng trong lúc Student đang chuẩn bị thông tin bổ sung.
- Student cố gắng gửi Feedback nhiều lần cho cùng một Request.

**Related**

- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Workflow: [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- Workflow: [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)

---

## 2. Staff Workspace

### FR-STA-01 – Request Classification and Assignment

**Description**

Staff có thể phân loại Request, xác định mức độ ưu tiên và chuyển Request đến Department hoặc người chịu trách nhiệm phù hợp.

**Actor**

- Primary Actor: Staff

**Priority**

- High – Đảm bảo Request được chuyển đến đúng đơn vị và có người chịu trách nhiệm xử lý.

**Preconditions**

- Staff đã đăng nhập.
- Staff có quyền thực hiện Classification and Assignment.
- Request đã được tiếp nhận thành công.

**Main Flow**

1. Staff truy cập danh sách Request cần phân loại.
2. Hệ thống hiển thị các Request chưa được phân công hoặc cần phân loại.
3. Staff xem nội dung và thông tin của Request.
4. Staff xác định Request Type.
5. Hệ thống lưu Priority phù hợp cho Request dựa trên mức độ ảnh hưởng và tính cấp thiết của yêu cầu.
6. Staff lựa chọn Department tiếp nhận.
7. Staff chỉ định người chịu trách nhiệm.
8. Staff xác nhận việc phân công.
9. Hệ thống lưu thông tin phân loại và Assignment.
10. Hệ thống ghi nhận hoạt động và cập nhật thông tin Request.

**Business Rules**

- BR-01: Mỗi Request phải được phân loại theo Request Type phù hợp.
- BR-02: Priority của mỗi Request được xác định dựa trên mức độ ảnh hưởng và tính cấp thiết của yêu cầu. Priority là thuộc tính của Request, không phải một bước độc lập trong quy trình xử lý.
- BR-03: Request phải được phân công đến Department phù hợp.
- BR-04: Request được phân công phải có người chịu trách nhiệm cụ thể.
- BR-05: Các thay đổi liên quan đến Classification và Assignment phải được ghi nhận.

**Alternative and Error Flows**

- AF-01: Staff có thể thay đổi Department hoặc người chịu trách nhiệm khi Request chưa được xử lý hoặc cần phân công lại.
- AF-02: Request có thể được phân công lại khi có sự thay đổi về nguồn lực hoặc trách nhiệm.
- EF-01: Nếu chưa xác định được Department phù hợp, hệ thống không xác nhận việc phân công.
- EF-02: Nếu người được chỉ định không thuộc phạm vi phân công hợp lệ, hệ thống thông báo lỗi.
- EF-03: Nếu thông tin phân loại chưa đầy đủ, hệ thống yêu cầu Staff hoàn thiện trước khi xác nhận.

**Acceptance Criteria**

- FR-STA-01/AC-01: Staff có thể xem các Request cần phân loại.
- FR-STA-01/AC-02: Staff có thể xác định Request Type và Priority.
- FR-STA-01/AC-03: Staff có thể phân công Request đến Department phù hợp.
- FR-STA-01/AC-04: Staff có thể chỉ định người chịu trách nhiệm cho Request.
- FR-STA-01/AC-05: Hệ thống không xác nhận Assignment khi thiếu thông tin phân công bắt buộc.
- FR-STA-01/AC-06: Hệ thống ghi nhận lịch sử thay đổi Classification và Assignment.

**Edge Cases**

- Request không thể xác định Department phù hợp ngay từ đầu.
- Một Department có nhiều Staff có thể tiếp nhận Request.
- Request cần được phân công lại sau khi đã có người chịu trách nhiệm.
- Staff cố gắng phân công Request cho tài khoản không còn quyền xử lý.

**Related**

- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Workflow: [WF-02 – Classify and Assign](../04-workflows/WF-02-classify-and-assign.md)
- Workflow: [WF-05 – Transfer Request](../04-workflows/WF-05-transfer-request.md)

---

### FR-STA-02 – Queue Management

**Description**

Staff có thể xem và quản lý danh sách Request được phân công cho cá nhân hoặc Department thông qua một hàng đợi tập trung.

**Actor**

- Primary Actor: Staff

**Priority**

- High – Giúp Staff quản lý khối lượng công việc và xác định các Request cần ưu tiên xử lý.

**Preconditions**

- Staff đã đăng nhập.
- Staff có quyền truy cập Staff Workspace.
- Hệ thống có các Request được tiếp nhận.

**Main Flow**

1. Staff truy cập Staff Workspace.
2. Hệ thống hiển thị danh sách Request thuộc phạm vi được phân công.
3. Staff xem thông tin tổng quan của từng Request.
4. Staff lọc danh sách theo Status hoặc Priority.
5. Staff lựa chọn Request cần xử lý.
6. Hệ thống hiển thị thông tin chi tiết của Request.
7. Staff tiếp tục xử lý Request theo quy trình.

**Business Rules**

- BR-01: Staff chỉ được xem Request thuộc phạm vi được cấp quyền.
- BR-02: Request trong hàng đợi phải hiển thị Status và Priority.
- BR-03: Hệ thống phải thể hiện thời gian chờ của Request.
- BR-04: Danh sách Request phải phản ánh các cập nhật mới nhất đã được ghi nhận.

**Alternative and Error Flows**

- AF-01: Staff có thể thay đổi điều kiện lọc để tìm Request khác.
- AF-02: Nếu không có Request phù hợp với điều kiện lọc, hệ thống hiển thị thông báo không có kết quả.
- EF-01: Nếu Staff cố gắng truy cập Request ngoài phạm vi được cấp quyền, hệ thống từ chối truy cập.
- EF-02: Nếu không thể tải danh sách Request, hệ thống thông báo lỗi và cho phép thử lại.

**Acceptance Criteria**

- FR-STA-02/AC-01: Staff có thể xem danh sách Request thuộc phạm vi được phân công.
- FR-STA-02/AC-02: Hệ thống hiển thị Status và Priority của từng Request.
- FR-STA-02/AC-03: Staff có thể lọc Request theo Status.
- FR-STA-02/AC-04: Staff có thể lọc Request theo Priority.
- FR-STA-02/AC-05: Hệ thống hiển thị thời gian chờ của Request.
- FR-STA-02/AC-06: Staff không thể xem Request ngoài phạm vi quyền truy cập.

**Edge Cases**

- Department chưa có Request nào được phân công.
- Nhiều Request có cùng Priority.
- Request thay đổi Status trong khi Staff đang xem danh sách.
- Staff truy cập một Request vừa được chuyển sang Department khác.

**Related**

- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Workflow: [WF-02 – Classify and Assign](../04-workflows/WF-02-classify-and-assign.md)
- Workflow: [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)

---

### FR-STA-03 – Request Processing, Transfer and Resolution

**Description**

Staff có thể xử lý Request, cập nhật tiến độ, ghi nhận hoạt động, yêu cầu bổ sung thông tin, chuyển Request sang Department khác và đóng Request khi vấn đề được giải quyết.

**Actor**

- Primary Actor: Staff
- Supporting Actor: Student

**Priority**

- High – Đây là chức năng cốt lõi để giải quyết các yêu cầu hỗ trợ của sinh viên.

**Preconditions**

- Staff đã đăng nhập.
- Request đã được tiếp nhận và phân công.
- Staff có quyền xử lý Request tương ứng.

**Main Flow**

1. Staff truy cập Request được phân công.
2. Hệ thống hiển thị thông tin và lịch sử xử lý.
3. Staff kiểm tra nội dung Request.
4. Staff thực hiện các hoạt động xử lý cần thiết.
5. Staff cập nhật Status theo tiến độ thực tế.
6. Staff ghi nhận nội dung xử lý vào Activity Log.
7. Nếu cần, Staff yêu cầu Student bổ sung thông tin.
8. Nếu cần chuyển đơn vị xử lý, Staff thực hiện Transfer Request.
9. Khi vấn đề được giải quyết, Staff cập nhật kết quả.
10. Staff đóng Request.
11. Hệ thống lưu lại kết quả và lịch sử xử lý.

**Business Rules**

- BR-01: Staff chỉ được xử lý Request thuộc phạm vi quyền hạn của mình.
- BR-02: Status phải phản ánh đúng tình trạng xử lý hiện tại.
- BR-03: Mọi hoạt động xử lý quan trọng phải được ghi nhận.
- BR-04: Khi yêu cầu bổ sung thông tin, Request phải thể hiện rõ tình trạng chờ thông tin.
- BR-05: Khi Transfer Request, thông tin và lịch sử xử lý phải được bảo toàn.
- BR-06: Request chỉ được đóng khi vấn đề đã được giải quyết theo quy trình.
- BR-07: Hoạt động Escalation phải được ghi nhận khi Request cần chuyển cấp xử lý.
- BR-08: Khi Student cung cấp đầy đủ thông tin được yêu cầu, Request có thể chuyển từ trạng thái "Chờ bổ sung thông tin" trở lại "Đang xử lý".

**Alternative and Error Flows**

- AF-01: Staff có thể yêu cầu Student bổ sung thông tin trước khi tiếp tục xử lý.
- AF-02: Staff có thể Transfer Request sang Department khác khi cần chuyên môn hoặc thẩm quyền phù hợp.
- AF-03: Staff có thể Escalate Request khi vấn đề vượt quá phạm vi xử lý thông thường.
- AF-04: Staff có thể tiếp tục xử lý Request sau khi nhận được thông tin bổ sung.
- EF-01: Nếu Staff không có quyền xử lý Request, hệ thống từ chối thao tác.
- EF-02: Nếu Status không hợp lệ với quy trình, hệ thống không chấp nhận cập nhật.
- EF-03: Nếu không xác định được Department tiếp nhận khi Transfer, hệ thống không hoàn tất thao tác.
- EF-04: Nếu Request chưa đáp ứng điều kiện giải quyết, hệ thống không cho phép đóng Request.

**Acceptance Criteria**

- FR-STA-03/AC-01: Staff có thể xem nội dung và lịch sử xử lý của Request được phân công.
- FR-STA-03/AC-02: Staff có thể cập nhật Status của Request.
- FR-STA-03/AC-03: Staff có thể ghi nhận nội dung xử lý vào Activity Log.
- FR-STA-03/AC-04: Staff có thể yêu cầu Student bổ sung thông tin.
- FR-STA-03/AC-05: Hệ thống cập nhật trạng thái phù hợp khi Request chờ thông tin bổ sung.
- FR-STA-03/AC-06: Staff có thể Transfer Request sang Department khác.
- FR-STA-03/AC-07: Hệ thống bảo toàn thông tin và lịch sử xử lý sau khi Transfer.
- FR-STA-03/AC-08: Staff có thể Escalate Request theo quy trình.
- FR-STA-03/AC-09: Hệ thống không cho phép đóng Request khi chưa đáp ứng điều kiện giải quyết.
- FR-STA-03/AC-10: Hệ thống ghi nhận thời điểm và người thực hiện các hoạt động xử lý.
- FR-STA-03/AC-11: Hệ thống cho phép Request chuyển từ "Chờ bổ sung thông tin" sang "Đang xử lý" sau khi Student cung cấp đầy đủ thông tin được yêu cầu.

**Edge Cases**

- Student không cung cấp thông tin bổ sung trong thời gian dự kiến.
- Request được Transfer nhiều lần giữa các Department.
- Request được cập nhật bởi hai Staff trong cùng khoảng thời gian.
- Staff cố gắng đóng Request khi vẫn còn thông tin cần xử lý.
- Request cần Escalation nhưng chưa xác định được đơn vị tiếp nhận.

**Related**

- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Workflow: [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)
- Workflow: [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- Workflow: [WF-05 – Transfer Request](../04-workflows/WF-05-transfer-request.md)
- Workflow: [WF-06 – Resolve and Close](../04-workflows/WF-06-resolve-and-close.md)

---

## 3. Management Dashboard

### FR-MGT-01 – Request Monitoring and Overdue Alerts

**Description**

Management có thể theo dõi tình hình tiếp nhận và xử lý Request thông qua Dashboard, đồng thời nhận biết các Request đang chờ xử lý hoặc vượt quá thời gian xử lý dự kiến.

**Actor**

- Primary Actor: Management

**Priority**

- Medium – Giúp Ban Quản Lý giám sát tình hình xử lý và nhận biết các vấn đề cần can thiệp.

**Preconditions**

- Management đã đăng nhập.
- Management có quyền truy cập Management Dashboard.
- Hệ thống có dữ liệu Request để tổng hợp.

**Main Flow**

1. Management truy cập Management Dashboard.
2. Hệ thống tổng hợp dữ liệu Request.
3. Hệ thống hiển thị số lượng Request mới.
4. Hệ thống hiển thị số lượng Request đang xử lý.
5. Hệ thống hiển thị danh sách Request quá hạn.
6. Management xem chi tiết các Request cần theo dõi.
7. Hệ thống hiển thị cảnh báo đối với các Request vượt quá thời gian xử lý dự kiến.

**Business Rules**

- BR-01: Dữ liệu Dashboard phải được tổng hợp từ các Request đã được ghi nhận trong hệ thống.
- BR-02: Request được xem là quá hạn khi vượt quá thời gian xử lý mục tiêu được cấu hình.
- BR-03: Management chỉ được xem dữ liệu thuộc phạm vi quyền truy cập.
- BR-04: Các số liệu tổng quan phải phản ánh trạng thái dữ liệu tại thời điểm truy vấn.

**Alternative and Error Flows**

- AF-01: Management có thể lựa chọn khoảng thời gian hoặc điều kiện lọc nếu Dashboard hỗ trợ.
- AF-02: Management có thể truy cập danh sách chi tiết từ số liệu tổng quan.
- EF-01: Nếu không có dữ liệu Request, hệ thống hiển thị các chỉ số bằng 0 hoặc thông báo phù hợp.
- EF-02: Nếu không thể tải dữ liệu tổng quan, hệ thống thông báo lỗi.
- EF-03: Nếu Management không có quyền truy cập, hệ thống từ chối truy cập Dashboard.

**Acceptance Criteria**

- FR-MGT-01/AC-01: Dashboard hiển thị tổng số Request mới.
- FR-MGT-01/AC-02: Dashboard hiển thị số lượng Request đang xử lý.
- FR-MGT-01/AC-03: Dashboard hiển thị danh sách Request quá hạn.
- FR-MGT-01/AC-04: Hệ thống xác định Request quá hạn dựa trên thời gian xử lý mục tiêu được cấu hình.
- FR-MGT-01/AC-05: Hệ thống hiển thị cảnh báo đối với Request quá hạn.
- FR-MGT-01/AC-06: Management có thể truy cập thông tin chi tiết trong phạm vi được cấp quyền.

**Edge Cases**

- Không có Request nào được ghi nhận.
- Request vừa được cập nhật Status trong khi Dashboard đang hiển thị.
- Request chưa có thời gian xử lý mục tiêu được cấu hình.
- Nhiều Request cùng vượt quá thời gian xử lý mục tiêu.

**Related**

- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)
- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)

---

### FR-MGT-02 – Performance and Management Reporting

**Description**

Management có thể xem các báo cáo và số liệu tổng hợp để đánh giá hiệu quả xử lý Request, phân bổ khối lượng công việc và chất lượng dịch vụ hỗ trợ sinh viên.

**Actor**

- Primary Actor: Management

**Priority**

- Medium – Cung cấp dữ liệu hỗ trợ Ban Quản Lý đánh giá và cải thiện hoạt động hỗ trợ sinh viên.

**Preconditions**

- Management đã đăng nhập.
- Management có quyền truy cập chức năng Reporting.
- Hệ thống có dữ liệu Request và các hoạt động xử lý liên quan.

**Main Flow**

1. Management truy cập chức năng Reporting.
2. Hệ thống tổng hợp dữ liệu Request.
3. Management lựa chọn loại báo cáo hoặc thông tin cần xem.
4. Hệ thống hiển thị thời gian xử lý trung bình.
5. Hệ thống hiển thị thống kê theo Request Type.
6. Hệ thống hiển thị khối lượng công việc theo Department.
7. Hệ thống hiển thị dữ liệu Feedback và mức độ hài lòng của Student.
8. Management xem và sử dụng báo cáo để đánh giá chất lượng dịch vụ.

**Business Rules**

- BR-01: Báo cáo phải được tổng hợp từ dữ liệu đã được ghi nhận trong hệ thống.
- BR-02: Thời gian xử lý phải được tính dựa trên thời điểm tiếp nhận và thời điểm giải quyết Request theo quy tắc thống nhất.
- BR-03: Thống kê Request Type phải phản ánh đúng loại yêu cầu đã được phân loại.
- BR-04: Workload phải được tổng hợp theo Department tương ứng.
- BR-05: Feedback phải được sử dụng làm dữ liệu phục vụ việc đánh giá chất lượng dịch vụ.

**Alternative and Error Flows**

- AF-01: Management có thể xem các nhóm báo cáo khác nhau tùy theo nhu cầu quản lý.
- AF-02: Management có thể lọc dữ liệu theo khoảng thời gian nếu hệ thống hỗ trợ.
- EF-01: Nếu chưa có đủ dữ liệu để tính toán chỉ số, hệ thống hiển thị thông báo phù hợp.
- EF-02: Nếu dữ liệu báo cáo không thể tải, hệ thống thông báo lỗi.
- EF-03: Nếu Management không có quyền truy cập báo cáo, hệ thống từ chối thao tác.

**Acceptance Criteria**

- FR-MGT-02/AC-01: Hệ thống cung cấp số liệu về thời gian xử lý Request.
- FR-MGT-02/AC-02: Hệ thống cung cấp thống kê Request theo Request Type.
- FR-MGT-02/AC-03: Hệ thống cung cấp thống kê khối lượng công việc theo Department.
- FR-MGT-02/AC-04: Hệ thống hiển thị dữ liệu Feedback phục vụ đánh giá chất lượng dịch vụ.
- FR-MGT-02/AC-05: Hệ thống tổng hợp dữ liệu báo cáo dựa trên các Request đã được ghi nhận.
- FR-MGT-02/AC-06: Hệ thống thông báo khi dữ liệu chưa đủ để tính toán một chỉ số.

**Edge Cases**

- Chưa có Request nào được giải quyết.
- Chưa có Feedback từ Student.
- Một Department chưa được phân công Request.
- Dữ liệu Request bị thiếu thời điểm tiếp nhận hoặc giải quyết.

**Related**

- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)
- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- Workflow: [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)

---

## 4. Security and Access

### FR-SEC-01 – User Authentication and Role-Based Access Control

**Description**

Hệ thống cung cấp cơ chế xác thực người dùng và kiểm soát quyền truy cập dựa trên Role nhằm đảm bảo mỗi nhóm người dùng chỉ có thể sử dụng các chức năng và dữ liệu được cấp phép.

**Actor**

- Primary Actor: Student
- Primary Actor: Staff
- Primary Actor: Management

**Priority**

- High – Là chức năng nền tảng để bảo vệ dữ liệu và kiểm soát hoạt động của toàn hệ thống.

**Preconditions**

- Người dùng có tài khoản hợp lệ trong hệ thống.
- Các Role và quyền truy cập đã được cấu hình.
- Hệ thống có cơ chế xác thực người dùng.

**Main Flow**

1. Người dùng truy cập hệ thống.
2. Hệ thống hiển thị giao diện đăng nhập.
3. Người dùng cung cấp thông tin xác thực.
4. Hệ thống kiểm tra thông tin đăng nhập.
5. Hệ thống xác định Role của người dùng.
6. Hệ thống cấp quyền truy cập tương ứng.
7. Người dùng truy cập các chức năng phù hợp với Role của mình.
8. Hệ thống kiểm tra quyền khi người dùng thực hiện các thao tác liên quan đến dữ liệu.
9. Management truy cập chức năng quản lý người dùng và vai trò theo quyền được cấp.
10. Hệ thống hiển thị thông tin người dùng và Role hiện tại.
11. Management cập nhật Role khi cần thiết.
12. Hệ thống lưu thay đổi và ghi nhận hoạt động liên quan.

**Business Rules**

- BR-01: Người dùng phải được xác thực trước khi truy cập các chức năng yêu cầu đăng nhập.
- BR-02: Mỗi người dùng phải được gán Role phù hợp.
- BR-03: Student chỉ được truy cập dữ liệu và chức năng dành cho Student.
- BR-04: Staff chỉ được truy cập dữ liệu và chức năng thuộc phạm vi trách nhiệm được cấp.
- BR-05: Management chỉ được truy cập chức năng và dữ liệu phục vụ giám sát, báo cáo theo quyền được cấp.
- BR-06: Quyền truy cập phải được kiểm tra đối với cả giao diện và các thao tác xử lý dữ liệu.

**Alternative and Error Flows**

- AF-01: Người dùng có thể đăng xuất khỏi hệ thống.
- AF-02: Người dùng có thể đăng nhập lại sau khi phiên đăng nhập hết hạn.
- EF-01: Nếu thông tin đăng nhập không hợp lệ, hệ thống từ chối đăng nhập.
- EF-02: Nếu tài khoản không có Role hợp lệ, hệ thống không cấp quyền truy cập.
- EF-03: Nếu người dùng cố truy cập chức năng ngoài quyền hạn, hệ thống từ chối thao tác.
- EF-04: Nếu phiên đăng nhập hết hạn, hệ thống yêu cầu xác thực lại.

**Acceptance Criteria**

- FR-SEC-01/AC-01: Người dùng phải đăng nhập thành công trước khi truy cập chức năng yêu cầu xác thực.
- FR-SEC-01/AC-02: Hệ thống xác định Role của người dùng sau khi xác thực thành công.
- FR-SEC-01/AC-03: Student không thể truy cập chức năng chỉ dành cho Staff hoặc Management.
- FR-SEC-01/AC-04: Staff chỉ có thể thực hiện các thao tác thuộc phạm vi được cấp quyền.
- FR-SEC-01/AC-05: Management chỉ có thể truy cập dữ liệu và chức năng theo quyền được cấp.
- FR-SEC-01/AC-06: Hệ thống từ chối thao tác truy cập trái phép.
- FR-SEC-01/AC-07: Hệ thống yêu cầu xác thực lại khi phiên đăng nhập hết hạn.
- FR-SEC-01/AC-08: Management có thể xem thông tin người dùng và Role hiện tại theo quyền được cấp.
- FR-SEC-01/AC-09: Management có thể cập nhật Role của người dùng theo quyền được cấp.

**Edge Cases**

- Người dùng đăng nhập bằng tài khoản không tồn tại.
- Người dùng cố truy cập chức năng bằng đường dẫn trực tiếp.
- Role của người dùng thay đổi trong quá trình sử dụng hệ thống.
- Người dùng cố tiếp tục thao tác sau khi đăng xuất.

**Related**

- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)

---

### FR-SEC-02 – Audit Logging and Data Access Protection

**Description**

Hệ thống ghi nhận các hoạt động quan trọng liên quan đến Request, thay đổi dữ liệu và truy cập thông tin nhằm hỗ trợ kiểm tra, giám sát và bảo vệ dữ liệu sinh viên.

**Actor**

- Primary Actor: System
- Supporting Actor: Staff
- Supporting Actor: Management

**Priority**

- High – Đảm bảo khả năng kiểm tra hoạt động và bảo vệ dữ liệu trong quá trình sử dụng hệ thống.

**Preconditions**

- Người dùng đã được xác thực.
- Hệ thống đã cấu hình quyền truy cập dữ liệu.
- Cơ chế ghi nhận hoạt động đã được thiết lập.

**Main Flow**

1. Người dùng thực hiện thao tác liên quan đến Request hoặc dữ liệu.
2. Hệ thống kiểm tra quyền truy cập của người dùng.
3. Hệ thống thực hiện thao tác nếu người dùng có quyền.
4. Hệ thống ghi nhận hoạt động cần thiết.
5. Hệ thống lưu thông tin về người thực hiện, thời điểm và loại hoạt động.
6. Người có quyền phù hợp có thể truy cập thông tin lịch sử để kiểm tra.

**Business Rules**

- BR-01: Các hoạt động quan trọng liên quan đến Request phải được ghi nhận.
- BR-02: Các thay đổi về Status, Priority, Assignment và thông tin xử lý phải có lịch sử.
- BR-03: Quyền truy cập dữ liệu sinh viên phải được giới hạn theo Role.
- BR-04: Tài liệu đính kèm phải được bảo vệ theo quyền truy cập của Request tương ứng.
- BR-05: Thông tin lịch sử truy cập và thay đổi chỉ được xem bởi người có thẩm quyền.
- BR-06: Dữ liệu phải được quản lý theo thời gian lưu trữ được quy định.
- BR-07: Prototype và testing sử dụng dữ liệu mô phỏng thay cho dữ liệu cá nhân thực tế.

**Alternative and Error Flows**

- AF-01: Người có quyền phù hợp có thể xem lịch sử hoạt động của Request.
- AF-02: Hệ thống có thể hiển thị thông tin lịch sử theo từng loại hoạt động.
- EF-01: Nếu người dùng không có quyền truy cập tài liệu đính kèm, hệ thống từ chối truy cập.
- EF-02: Nếu người dùng không có quyền xem Audit Log, hệ thống từ chối thao tác.
- EF-03: Nếu hoạt động không thể được ghi nhận, hệ thống xử lý theo chính sách kiểm soát lỗi và bảo đảm không xác nhận một thao tác quan trọng là hoàn tất khi chưa đáp ứng yêu cầu ghi nhận.

**Acceptance Criteria**

- FR-SEC-02/AC-01: Hệ thống ghi nhận các thay đổi quan trọng về Status của Request.
- FR-SEC-02/AC-02: Hệ thống ghi nhận các thay đổi về Priority và Assignment.
- FR-SEC-02/AC-03: Hệ thống ghi nhận người thực hiện, thao tác được thực hiện, thời điểm thực hiện và các thay đổi liên quan đến Request.
- FR-SEC-02/AC-04: Student không thể truy cập tài liệu đính kèm thuộc Request của người dùng khác.
- FR-SEC-02/AC-05: Staff chỉ được truy cập tài liệu thuộc phạm vi được phân công.
- FR-SEC-02/AC-06: Chỉ người dùng có quyền phù hợp mới được xem Audit Log.
- FR-SEC-02/AC-07: Dữ liệu được quản lý theo chính sách lưu trữ đã cấu hình.
- FR-SEC-02/AC-08: Prototype và testing sử dụng dữ liệu mô phỏng thay cho dữ liệu cá nhân thực tế.

**Edge Cases**

- Người dùng cố truy cập trực tiếp URL của tài liệu đính kèm.
- Một Request được cập nhật nhiều lần liên tiếp.
- Một hoạt động bị gián đoạn trong lúc hệ thống đang ghi nhận lịch sử.
- Người dùng không còn quyền truy cập nhưng vẫn giữ đường dẫn đến Audit Log.
- Dữ liệu mô phỏng chứa thông tin có hình thức giống dữ liệu cá nhân thực tế.

**Related**

- Module: [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- Module: [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- Module: [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- Module: [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)

---

## 5. Requirement Summary

| Module | Requirement ID | Functional Requirement | Priority |
|---|---|---|---|
| M01 | FR-STU-01 | Request Submission | High |
| M01 | FR-STU-02 | Request Tracking and Notifications | High |
| M01 | FR-STU-03 | Additional Information and Feedback | High |
| M02 | FR-STA-01 | Request Classification and Assignment | High |
| M02 | FR-STA-02 | Queue Management | High |
| M02 | FR-STA-03 | Request Processing, Transfer and Resolution | High |
| M03 | FR-MGT-01 | Request Monitoring and Overdue Alerts | High |
| M03 | FR-MGT-02 | Performance and Management Reporting | High |
| M04 | FR-SEC-01 | User Authentication and Role-Based Access Control | High |
| M04 | FR-SEC-02 | Audit Logging and Data Access Protection | High |

## 6. Requirement Traceability

Các Functional Requirements được liên kết với Module và Workflow tương ứng để hỗ trợ việc quản lý yêu cầu và kiểm thử.

| Requirement ID | Related Workflow |
|---|---|
| FR-STU-01 | WF-01 |
| FR-STU-02 | WF-01, WF-06 |
| FR-STU-03 | WF-04, WF-07 |
| FR-STA-01 | WF-02, WF-05 |
| FR-STA-02 | WF-02, WF-03 |
| FR-STA-03 | WF-03, WF-04, WF-05, WF-06 |
| FR-MGT-01 | Management Monitoring |
| FR-MGT-02 | Management Reporting, WF-07 |
| FR-SEC-01 | Security and Access Control |
| FR-SEC-02 | Security, Audit Logging and Data Protection |

Các mã Acceptance Criteria được sử dụng làm cơ sở xây dựng Test Scenarios trong tài liệu `06-acceptance/test-scenarios.md` và Traceability Matrix trong `06-acceptance/traceability-matrix.md`.

## 7. Scope Limitations

Các chức năng được mô tả trong tài liệu này phục vụ phạm vi thiết kế và phát triển prototype của UniSupport.

Những nội dung sau chưa thuộc phạm vi ưu tiên của phiên bản hiện tại:

- Xử lý hoặc thanh toán học phí.
- Thay thế hệ thống quản lý học tập hoặc quản lý học vụ.
- Tự động đưa ra quyết định học vụ.
- Tích hợp đầy đủ với tất cả hệ thống hiện có của trường.
- Triển khai hệ thống production hoàn chỉnh trên quy mô toàn trường.

Các chức năng bổ sung có thể được xem xét trong future roadmap nếu thời gian, nguồn lực và điều kiện thực tế cho phép.