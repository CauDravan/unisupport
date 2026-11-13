# Acceptance Criteria

## 1. Purpose

Tài liệu này xác định các tiêu chí dùng để đánh giá liệu Interactive Prototype của UniSupport có đáp ứng các yêu cầu chức năng cơ bản hay không.

Việc nghiệm thu được thực hiện thông qua Interactive Prototype, Test Scenarios và Usability Testing sử dụng dữ liệu giả lập.

Prototype được xem là đáp ứng yêu cầu khi các kịch bản chính có thể được thực hiện thành công và tạo ra Expected Result đã xác định.

## 2. Acceptance Criteria

| ID | Scenario | Expected Result | Related Requirements |
|---|---|---|---|
| AC-01 | Student gửi yêu cầu đầy đủ | Request được tạo thành công và Student nhận được Request ID / Tracking ID để theo dõi. | FR-STU-01 |
| AC-02 | Student gửi yêu cầu thiếu thông tin bắt buộc | Hệ thống xác định và hiển thị các trường thông tin bắt buộc còn thiếu. Request chưa được tạo cho đến khi Student bổ sung đầy đủ thông tin. | FR-STU-01 |
| AC-03 | Staff nhận Request mới | Request mới xuất hiện trong Queue tương ứng để Staff có thể xem và tiếp nhận xử lý. | FR-STA-01, FR-STA-02 |
| AC-04 | Staff phân công Request | Department hoặc Staff chịu trách nhiệm được ghi nhận trên Request và có thể được kiểm tra trong thông tin Request. | FR-STA-01 |
| AC-05 | Staff thay đổi Request Status | Status mới được lưu và hiển thị cho các User có quyền truy cập phù hợp. | FR-STA-03 |
| AC-06 | Staff yêu cầu Student bổ sung thông tin | Yêu cầu bổ sung thông tin được ghi nhận và Student nhận được thông báo để thực hiện bổ sung. | FR-STA-03, FR-STU-02 |
| AC-07 | Student cung cấp thông tin bổ sung | Thông tin bổ sung được lưu vào Request và Staff có thể tiếp tục xử lý Request. | FR-STU-03 |
| AC-08 | Staff chuyển giao Request | Department hoặc Staff tiếp nhận mới được ghi nhận. Thông tin Request và lịch sử xử lý trước khi chuyển giao được bảo toàn. | FR-STA-03 |
| AC-09 | Staff hoàn tất và đóng Request | Request được cập nhật sang trạng thái Closed sau khi hoàn tất quy trình giải quyết theo Workflow đã thống nhất. | FR-STA-03 |
| AC-10 | Student kiểm tra Request | Student có thể xem Status hiện tại và lịch sử cập nhật được phép truy cập của Request. | FR-STU-02 |
| AC-11 | Management mở Management Dashboard | Dashboard hiển thị các số liệu tổng quan về Request, bao gồm số lượng Request mới, đang xử lý và quá hạn khi có dữ liệu tương ứng. | FR-MGT-01 |
| AC-12 | User không được cấp quyền cố gắng truy cập chức năng hoặc dữ liệu | Hệ thống từ chối truy cập và không cho phép User thực hiện hành động nằm ngoài quyền được cấp. | FR-SEC-01, FR-SEC-02 |
| AC-13 | User thực hiện hành động cần được ghi nhận | Hoạt động được ghi vào Activity Log hoặc Request History để phục vụ việc theo dõi và kiểm tra. | FR-STA-03, FR-SEC-02 |
| AC-14 | Student gửi Feedback sau khi Request được xử lý | Feedback được lưu và liên kết với Request tương ứng để có thể sử dụng trong việc đánh giá hoặc báo cáo phù hợp. | FR-STU-03, FR-MGT-02 |

**Note:**

- Cột `Related Requirements` thể hiện mối liên hệ ở cấp Functional Requirement, không có nghĩa mỗi AC tổng quát tương ứng chính xác với một AC riêng trong FR.
- Các AC chi tiết theo từng FR vẫn được duy trì trong `functional-requirements.md`.
- Các trường hợp chưa có quy tắc nghiệp vụ cụ thể cần được đối chiếu với Workflow và xác nhận trước khi dùng làm điều kiện Pass/Fail chính thức.

## 3. Acceptance Scope

Các tiêu chí trên tập trung vào những chức năng chính trong phạm vi prototype:

- **Student Request Submission:** Student gửi Request và nhận thông tin xác nhận.
- **Request Tracking:** Student theo dõi Status và thông tin cập nhật của Request.
- **Request Classification & Assignment:** Staff phân loại, phân công và xác định người hoặc bộ phận chịu trách nhiệm.
- **Request Processing:** Staff tiếp nhận, cập nhật, chuyển giao và hoàn tất Request.
- **Management & Reporting:** Management theo dõi số liệu và thông tin tổng quan về hoạt động hỗ trợ.
- **Security & Access Control:** Hệ thống kiểm soát quyền truy cập theo Role của User.

Các tiêu chí này nhằm kiểm chứng quy trình hỗ trợ cốt lõi:

**Submit → Classify → Assign → Process → Resolve → Feedback**

## 4. Acceptance Approach

Việc đánh giá các Acceptance Criteria được thực hiện thông qua những phương pháp sau:

### 4.1 Interactive Prototype

Kiểm tra các chức năng chính thông qua Interactive Prototype và các luồng tương tác được thiết kế cho Student, Staff và Management.

### 4.2 Test Scenarios

Thực hiện các Test Scenarios đại diện cho những tình huống chính trong quá trình gửi, phân công, xử lý, theo dõi và đóng Request.

Kết quả của từng Test Scenario được đối chiếu với Expected Result tương ứng để xác định Pass, Fail hoặc Blocked.

### 4.3 Usability Testing

Cho phép đại diện Student và Staff thực hiện các tác vụ chính trên prototype để đánh giá mức độ rõ ràng và dễ sử dụng.

### 4.4 Simulated Data

Sử dụng dữ liệu giả lập thay cho dữ liệu cá nhân thực tế trong quá trình kiểm thử và trình diễn prototype.

## 5. Acceptance Result

Một Acceptance Criteria được xem là **Accepted** khi:

- Kịch bản tương ứng có thể được thực hiện trên Interactive Prototype.
- Hệ thống tạo ra Expected Result đã xác định.
- Không phát sinh lỗi nghiêm trọng làm gián đoạn Workflow chính.
- Quyền truy cập được áp dụng phù hợp với Role của User.
- Dữ liệu và lịch sử xử lý cần thiết được duy trì trong quá trình thực hiện.

Kết quả nghiệm thu được ghi nhận riêng cho từng Acceptance Criteria trong quá trình Testing và Prototype Review.

Các trường hợp không thể kiểm thử do thiếu thông tin, thiếu dữ liệu hoặc chưa có quyết định từ Stakeholder cần được ghi nhận là **Blocked** thay vì tự động đánh giá là Accepted.