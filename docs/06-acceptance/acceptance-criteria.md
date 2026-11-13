# Acceptance Criteria

## 1. Purpose

Tài liệu này xác định các tiêu chí dùng để đánh giá liệu prototype UniSupport có đáp ứng các yêu cầu chức năng cơ bản hay không.

Việc nghiệm thu được thực hiện thông qua **Interactive Prototype**, các **test scenarios** và **Usability Testing** sử dụng dữ liệu giả lập.

Prototype được xem là đáp ứng yêu cầu khi các kịch bản chính được thực hiện thành công và cho ra kết quả mong đợi.

---

## 2. Acceptance Criteria

| ID        | Scenario                                                          | Expected Result                                                                                                 |
| --------- | ----------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| <a id="ac-01"></a>**AC-01** | Student gửi yêu cầu đầy đủ                                        | Request được tạo thành công và Student nhận được **Request ID / Tracking ID**.                                  |
| <a id="ac-02"></a>**AC-02** | Student gửi yêu cầu thiếu thông tin bắt buộc                      | Hệ thống xác định các thông tin còn thiếu và thông báo cho Student bổ sung trước khi tạo Request.               |
| <a id="ac-03"></a>**AC-03** | Staff nhận Request mới                                            | Request xuất hiện trong hàng chờ (**Queue**) tương ứng để Staff có thể tiếp nhận và xử lý.                      |
| <a id="ac-04"></a>**AC-04** | Staff phân công Request                                           | Bộ phận hoặc Staff chịu trách nhiệm được ghi nhận rõ ràng trên Request.                                         |
| <a id="ac-05"></a>**AC-05** | Staff thay đổi Request Status                                     | Status mới được ghi nhận và hiển thị cho các user có quyền truy cập phù hợp.                                    |
| <a id="ac-06"></a>**AC-06** | Staff yêu cầu Student bổ sung thông tin                           | Student nhận được thông báo rằng Request cần được bổ sung thông tin.                                            |
| <a id="ac-07"></a>**AC-07** | Student cung cấp thông tin bổ sung                                | Request có thể tiếp tục được xử lý sau khi Student cung cấp đầy đủ thông tin cần thiết.                         |
| <a id="ac-08"></a>**AC-08** | Staff chuyển giao Request                                         | Việc phân công mới được ghi nhận và lịch sử xử lý trước đó được bảo toàn.                                       |
| <a id="ac-09"></a>**AC-09** | Staff hoàn tất và đóng Request                                    | Request được chuyển sang trạng thái **Đã đóng (Closed)** sau khi vấn đề được giải quyết.                        |
| <a id="ac-10"></a>**AC-10** | Student kiểm tra Request                                          | Student có thể xem Request Status hiện tại và các thông tin cập nhật phù hợp.                                   |
| <a id="ac-11"></a>**AC-11** | Management mở Management Dashboard                                | Dashboard hiển thị các số liệu tổng quan về Request, bao gồm số lượng mới, đang xử lý và quá hạn.               |
| <a id="ac-12"></a>**AC-12** | User không được cấp quyền cố gắng truy cập chức năng hoặc dữ liệu | Hệ thống từ chối quyền truy cập và không cho phép User thực hiện hành động trái với role của mình.              |
| <a id="ac-13"></a>**AC-13** | User thực hiện một hành động cần được ghi nhận                    | Hoạt động liên quan được ghi lại trong **Activity Log / Request History** để phục vụ việc theo dõi và kiểm tra. |
| <a id="ac-14"></a>**AC-14** | Student gửi Feedback sau khi Request được xử lý                   | Feedback được lưu trữ và có thể được sử dụng cho các báo cáo hoặc đánh giá phù hợp.                             |

---

## 3. Acceptance Scope

Các tiêu chí trên tập trung vào những chức năng chính trong phạm vi prototype:

* **Student Request Submission**
* **Request Tracking**
* **Request Classification & Assignment**
* **Request Processing**
* **Management & Reporting**
* **Security & Access Control**

Các tiêu chí này nhằm kiểm chứng quy trình hỗ trợ cốt lõi:

**Submit → Classify → Assign → Process → Resolve → Feedback**

---

## 4. Acceptance Approach

Việc đánh giá các tiêu chí nghiệm thu sẽ được thực hiện bằng:

### 4.1. Interactive Prototype

Kiểm tra các chức năng chính thông qua prototype và các luồng tương tác được thiết kế cho Student, Staff và Management.

### 4.2. Test Scenarios

Thực hiện các kịch bản đại diện cho những tình huống chính trong quá trình gửi, phân công, xử lý, theo dõi và đóng Request.

### 4.3. Usability Testing

Cho phép đại diện Student và Staff thực hiện các tác vụ chính trên prototype để đánh giá mức độ rõ ràng và dễ sử dụng.

### 4.4. Simulated Data

Sử dụng dữ liệu giả lập thay cho dữ liệu cá nhân thực tế trong quá trình kiểm thử và trình diễn prototype.

---

## 5. Acceptance Result

Một chức năng được xem là **Accepted** khi:

* Kịch bản tương ứng có thể được thực hiện trên prototype.
* Hệ thống tạo ra **Expected Result** đã xác định.
* Không phát sinh lỗi nghiêm trọng làm gián đoạn workflow chính.
* Quyền truy cập được áp dụng phù hợp với role của User.
* Dữ liệu và lịch sử xử lý cần thiết được duy trì trong quá trình thực hiện.

Kết quả nghiệm thu có thể được ghi nhận cho từng **Acceptance Criteria** trong quá trình testing và review prototype.
