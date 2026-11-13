# Product Scope

## 1. Product Scope Overview

UniSupport là hệ thống quản lý yêu cầu hỗ trợ sinh viên dành cho Aurora University. Sản phẩm hướng đến việc tập trung hóa quá trình tiếp nhận, phân loại, phân công, xử lý và theo dõi các yêu cầu hỗ trợ sinh viên trên một nền tảng thống nhất.

Trong giai đoạn hiện tại, UniSupport tập trung vào việc xây dựng prototype nhằm minh họa các chức năng và quy trình nghiệp vụ chính. Hệ thống phục vụ ba nhóm người dùng chính: Student, Staff và Management.

Product Scope được xác định dựa trên Project Goal, nhu cầu của các nhóm người dùng và phạm vi nghiệp vụ bắt buộc trong đề bài.

## 2. In Scope

Các chức năng dưới đây thuộc phạm vi sản phẩm UniSupport trong giai đoạn hiện tại.

### 2.1. Student Request Submission

Sinh viên có thể gửi yêu cầu hỗ trợ thông qua Student Portal. Khi tạo yêu cầu, sinh viên cung cấp các thông tin cần thiết để nhân viên có thể xem xét và xử lý.

Các chức năng bao gồm:

- Cho phép Student tạo và gửi yêu cầu hỗ trợ.
- Cho phép Student lựa chọn Request Type phù hợp với vấn đề cần hỗ trợ.
- Cho phép Student nhập Subject và Description.
- Cho phép Student đính kèm tài liệu liên quan nếu cần.
- Kiểm tra các trường thông tin bắt buộc trước khi tiếp nhận yêu cầu.
- Tạo Request ID duy nhất cho mỗi yêu cầu được tiếp nhận.
- Hiển thị thông báo xác nhận khi yêu cầu được gửi thành công.

**Primary Actor:** Student.

**Expected Outcome:** Yêu cầu được hệ thống tiếp nhận, lưu trữ và có Request ID để phục vụ việc theo dõi trong các bước tiếp theo.

### 2.2. Request Classification & Assignment

Hệ thống hỗ trợ Staff phân loại yêu cầu và xác định bộ phận hoặc nhân viên chịu trách nhiệm xử lý.

Các chức năng bao gồm:

- Cho phép Staff xem xét thông tin của yêu cầu đã được tiếp nhận.
- Phân loại yêu cầu dựa trên nội dung và Request Type.
- Xác định Department phù hợp để xử lý yêu cầu.
- Xác định mức độ ưu tiên của yêu cầu.
- Phân công yêu cầu cho Staff chịu trách nhiệm.
- Ghi nhận thông tin Department và Assigned Staff.
- Hỗ trợ chuyển yêu cầu khi được xác định không thuộc phạm vi xử lý hiện tại.
- Ghi nhận các thay đổi liên quan đến classification và assignment vào Request History.

**Primary Actor:** Staff.

**Expected Outcome:** Yêu cầu được phân loại và xác định nơi chịu trách nhiệm xử lý, giúp hạn chế tình trạng yêu cầu bị bỏ sót hoặc không rõ người phụ trách.

### 2.3. Request Processing

Staff có thể tiếp nhận và xử lý các yêu cầu được phân công thông qua Staff Workspace.

Các chức năng bao gồm:

- Cho phép Staff xem danh sách yêu cầu được giao.
- Xem nội dung, thông tin và tài liệu đính kèm của yêu cầu.
- Cập nhật Request Status trong quá trình xử lý.
- Ghi nhận các hoạt động và thông tin xử lý.
- Yêu cầu Student bổ sung thông tin hoặc tài liệu khi cần thiết.
- Chuyển yêu cầu sang Staff hoặc Department khác khi cần thiết.
- Ghi nhận thông tin chuyển giao và lý do chuyển giao.
- Lưu giữ lịch sử xử lý trong quá trình chuyển giao.
- Ghi nhận kết quả giải quyết yêu cầu.
- Đóng yêu cầu sau khi hoàn tất xử lý theo quy trình.

**Primary Actor:** Staff.

**Expected Outcome:** Yêu cầu được xử lý theo quy trình thống nhất, có người chịu trách nhiệm và có lịch sử hoạt động để phục vụ việc theo dõi.

### 2.4. Request Tracking

Hệ thống cho phép Student theo dõi tình trạng và tiến độ xử lý các yêu cầu đã gửi.

Các chức năng bao gồm:

- Hiển thị danh sách các yêu cầu Student đã gửi.
- Cho phép Student xem thông tin chi tiết của từng yêu cầu.
- Hiển thị Request Status hiện tại.
- Hiển thị lịch sử cập nhật và xử lý phù hợp.
- Thông báo cho Student khi trạng thái hoặc tiến trình xử lý thay đổi.
- Thông báo khi Staff yêu cầu bổ sung thông tin.
- Cho phép Student cung cấp thông tin bổ sung.
- Cho phép Student xem kết quả xử lý sau khi yêu cầu được hoàn tất.
- Cho phép Student gửi Feedback về kết quả hỗ trợ sau khi yêu cầu được đóng.

**Primary Actor:** Student.

**Expected Outcome:** Student có thể chủ động theo dõi yêu cầu, biết tình trạng xử lý và thực hiện các hành động cần thiết mà không phải liên hệ nhiều lần để hỏi tiến độ.

### 2.5. Management & Reporting

Hệ thống cung cấp Dashboard và các báo cáo giúp Management theo dõi tình hình xử lý yêu cầu hỗ trợ sinh viên.

Các chức năng bao gồm:

- Hiển thị tổng số yêu cầu mới.
- Hiển thị số lượng yêu cầu đang được xử lý.
- Theo dõi số lượng yêu cầu quá hạn.
- Hiển thị tình trạng xử lý của các yêu cầu.
- Theo dõi thời gian xử lý trung bình theo từng Department.
- Theo dõi khối lượng yêu cầu được xử lý.
- Thống kê các loại yêu cầu phổ biến.
- Hiển thị dữ liệu Feedback từ Student.
- Cung cấp thông tin hỗ trợ Management đánh giá chất lượng hoạt động hỗ trợ sinh viên.

**Primary Actor:** Management.

**Expected Outcome:** Management có thể theo dõi khối lượng công việc, nhận biết các yêu cầu cần chú ý và sử dụng dữ liệu tổng hợp để đánh giá hoạt động hỗ trợ sinh viên.

### 2.6. Security & Privacy

Hệ thống phải xem xét việc bảo vệ thông tin người dùng và kiểm soát quyền truy cập trong toàn bộ các chức năng của UniSupport.

Các chức năng và yêu cầu bao gồm:

- Hỗ trợ xác thực người dùng.
- Phân quyền truy cập dựa trên vai trò Student, Staff và Management.
- Giới hạn quyền truy cập chức năng theo vai trò được cấp.
- Student chỉ được truy cập các yêu cầu thuộc tài khoản của mình.
- Staff chỉ được truy cập các yêu cầu thuộc phạm vi được phân công hoặc phạm vi quyền được cấp.
- Management truy cập Dashboard, báo cáo và chức năng quản lý theo quyền được cấp.
- Bảo vệ thông tin và tài liệu đính kèm của yêu cầu.
- Ghi nhận các hoạt động và thay đổi quan trọng thông qua Activity Logging.
- Xem xét thời gian lưu trữ dữ liệu và cách xử lý thông tin nhạy cảm.

**Primary Actors:** Student, Staff và Management.

**Expected Outcome:** Dữ liệu sinh viên được bảo vệ và người dùng chỉ có thể truy cập các chức năng, thông tin phù hợp với quyền được cấp.

## 3. Out of Scope

Trong giai đoạn hiện tại, các nội dung dưới đây chưa thuộc phạm vi triển khai chính của UniSupport. Một số nội dung có thể được xem xét trong Future Roadmap nếu có nhu cầu, thời gian và nguồn lực phù hợp.

### 3.1. Full System Integration

Không triển khai tích hợp thực tế với toàn bộ hệ thống hiện có của Aurora University.

UniSupport tập trung minh họa quy trình quản lý yêu cầu độc lập trong phạm vi prototype.

### 3.2. Real Personal Data

Không sử dụng dữ liệu cá nhân thật của sinh viên trong quá trình phát triển prototype và testing.

Các hoạt động kiểm thử sử dụng dữ liệu giả lập (Simulated Data).

### 3.3. Academic Management Replacement

Không thay thế hệ thống quản lý đào tạo hoặc các hệ thống quản lý học vụ hiện có của nhà trường.

UniSupport chỉ tập trung vào việc quản lý các yêu cầu hỗ trợ sinh viên.

### 3.4. Tuition Payment

Không triển khai chức năng thanh toán học phí hoặc xử lý giao dịch tài chính.

Các yêu cầu liên quan đến học phí chỉ được xem xét dưới góc độ yêu cầu hỗ trợ và trao đổi thông tin.

### 3.5. Automated Academic Decisions

Không xây dựng chức năng tự động đưa ra quyết định học vụ cho sinh viên.

Các quyết định liên quan đến học vụ vẫn thuộc trách nhiệm của các đơn vị có thẩm quyền.

### 3.6. University-wide Production Deployment

Không triển khai hệ thống production hoàn chỉnh trên quy mô toàn trường trong giai đoạn hiện tại.

Phạm vi tập trung vào prototype để minh họa chức năng, quy trình nghiệp vụ và hỗ trợ đánh giá giải pháp.

## 4. Scope Boundaries and Constraints

Việc thiết kế và phát triển UniSupport cần tuân thủ các giới hạn sau:

- **Project Duration:** Kế hoạch dự án có tổng thời gian 15 tuần.
- **Effort Limit:** Tổng ngân sách lao động tối đa là 320 person-hours.
- **User Groups:** Phải xem xét ít nhất ba vai trò Student, Staff và Management trong phạm vi các chức năng tương ứng.
- **Supported Devices:** Giải pháp phải xem xét khả năng sử dụng trên máy tính và thiết bị di động.
- **Localization:** Giải pháp phải xem xét hỗ trợ tiếng Việt và tiếng Anh.
- **Test Data:** Prototype và testing sử dụng dữ liệu giả lập.
- **Usability:** Giao diện và quy trình cần phù hợp với người dùng có mức độ thành thạo công nghệ khác nhau.
- **Security:** Quyền truy cập và dữ liệu sinh viên phải được bảo vệ theo vai trò và quyền được cấp.

Các chi tiết về Functional Requirements, Non-Functional Requirements, Business Rules và Acceptance Criteria được mô tả trong những tài liệu liên quan.

## 5. Related Documents

| Document | Purpose |
|---|---|
| [Product Overview](./README.md) | Giới thiệu tổng quan về UniSupport. |
| [Problem Statement](./problem-statement.md) | Mô tả các vấn đề của Student, Staff và Management. |
| [Product Goals](./product-goals.md) | Xác định mục tiêu và kết quả mong đợi của sản phẩm. |
| [Product Backlog](./product-backlog.md) | Danh sách chức năng và mức độ ưu tiên của sản phẩm. |
| [Users and Roles](../02-domain/users-and-roles.md) | Xác định nhóm người dùng và trách nhiệm của từng vai trò. |
| [Module PRDs](../03-modules/README.md) | Mô tả chức năng chi tiết của từng Module. |
| [Workflows](../04-workflows/) | Mô tả các quy trình nghiệp vụ của UniSupport. |
| [Functional Requirements](../05-requirements/functional-requirements.md) | Xác định các yêu cầu chức năng. |
| [Non-Functional Requirements](../05-requirements/non-functional-requirements.md) | Xác định các yêu cầu phi chức năng. |
| [Acceptance Criteria](../06-acceptance/acceptance-criteria.md) | Xác định điều kiện chấp nhận cho các yêu cầu. |