# UniSupport – Student Support Management System Project

## 3. Project Goal

UniSupport hướng đến việc lập kế hoạch và thiết kế một giải pháp quản lý tập trung quá trình tiếp nhận, phân công, xử lý và theo dõi các yêu cầu hỗ trợ sinh viên tại Aurora University.

Dự án tập trung vào các mục tiêu chính sau:

- **Improve Student Support Experience:** Giúp sinh viên gửi yêu cầu hỗ trợ, nhận xác nhận tiếp nhận và theo dõi tiến độ xử lý dễ dàng.
- **Improve Request Management:** Giúp nhân viên tiếp nhận, phân loại, phân công và xử lý yêu cầu theo quy trình rõ ràng.
- **Improve Management Visibility:** Cung cấp thông tin tổng hợp để ban quản lý theo dõi tình trạng yêu cầu và đánh giá chất lượng dịch vụ hỗ trợ.
- **Reduce Request Handling Issues:** Hạn chế tình trạng yêu cầu bị bỏ sót, xử lý trùng lặp, chậm trễ hoặc không xác định được người chịu trách nhiệm.

Các mục tiêu này được thực hiện thông qua một quy trình quản lý Request thống nhất, kết hợp với các cơ chế kiểm soát truy cập và bảo vệ dữ liệu phù hợp.

## 4. Project Scope

### 4.1. In Scope

Giải pháp UniSupport được tổ chức thành bốn Module có chức năng liên kết với nhau. Mỗi Module đảm nhiệm một phần nghiệp vụ cụ thể trong quy trình quản lý yêu cầu hỗ trợ sinh viên.

#### A. M01 – Student Portal

Module dành cho Student, hỗ trợ quá trình gửi và theo dõi yêu cầu hỗ trợ.

Các chức năng bao gồm:

- Cho phép Student tạo và gửi Support Request.
- Cho phép Student lựa chọn Request Type phù hợp.
- Cung cấp Subject, Description và tài liệu đính kèm khi cần thiết.
- Tạo Request ID duy nhất và thông báo xác nhận sau khi Request được tiếp nhận thành công.
- Cho phép Student xem danh sách, chi tiết và Request Status của các yêu cầu đã gửi.
- Hiển thị lịch sử cập nhật phù hợp của Request.
- Nhận thông báo khi Request Status thay đổi.
- Cho phép Student cung cấp Additional Information khi Staff yêu cầu.
- Cho phép Student gửi Feedback sau khi Request được xử lý và chuyển sang trạng thái Closed.

**Expected Outcome:** Student có thể chủ động gửi và theo dõi Request, biết được tình trạng xử lý và cung cấp thông tin bổ sung khi cần thiết.

#### B. M02 – Staff Workspace

Module dành cho Staff, hỗ trợ quá trình tiếp nhận, phân loại, phân công và xử lý Request.

Các chức năng bao gồm:

- Hiển thị danh sách Request được phân công cho Staff hoặc Department trong phạm vi quyền truy cập.
- Cho phép Staff xem thông tin và tài liệu đính kèm của Request.
- Phân loại Request theo Request Type.
- Xác định Department và Assigned Staff chịu trách nhiệm xử lý.
- Xác định Priority cho từng Request.
- Cập nhật Request Status trong quá trình xử lý.
- Ghi nhận các hoạt động xử lý vào Request History.
- Yêu cầu Student bổ sung thông tin hoặc tài liệu khi cần thiết.
- Transfer Request sang Staff hoặc Department khác khi cần thiết.
- Ghi nhận Resolution và đóng Request sau khi hoàn thành xử lý.

**Expected Outcome:** Staff có thể quản lý và xử lý Request theo quy trình thống nhất, xác định rõ người chịu trách nhiệm và duy trì lịch sử xử lý trong suốt quá trình.

#### C. M03 – Management Dashboard

Module dành cho Management, hỗ trợ theo dõi và đánh giá hoạt động hỗ trợ sinh viên.

Các chức năng bao gồm:

- Theo dõi số lượng Request mới.
- Theo dõi số lượng Request đang được xử lý.
- Theo dõi Request quá hạn.
- Theo dõi thời gian xử lý trung bình.
- Thống kê Request theo Department và Request Type.
- Theo dõi khối lượng công việc của từng Department.
- Xem Feedback và mức độ hài lòng của Student.
- Cung cấp Dashboard và các báo cáo tổng hợp phục vụ việc đánh giá chất lượng dịch vụ.

**Expected Outcome:** Management có thể theo dõi tình hình xử lý Request, nhận biết các vấn đề phổ biến và sử dụng dữ liệu tổng hợp để hỗ trợ việc cải thiện hoạt động dịch vụ sinh viên.

#### D. M04 – Security and Access

Module nền tảng hỗ trợ kiểm soát quyền truy cập và bảo vệ dữ liệu trong toàn bộ hệ thống UniSupport.

Các chức năng và yêu cầu bao gồm:

- Hỗ trợ User Authentication.
- Áp dụng Role-Based Access Control cho Student, Staff và Management.
- Kiểm soát quyền truy cập chức năng và dữ liệu theo Role được cấp.
- Giới hạn quyền truy cập Request và Attachment theo phạm vi được phân công hoặc quyền được cấp.
- Bảo vệ thông tin và tài liệu đính kèm của Student.
- Ghi nhận các hoạt động quan trọng thông qua Activity Logging và Audit Trail.
- Xem xét Data Retention và Sensitive Data Handling.
- Sử dụng Simulated Data trong prototype và testing.

**Expected Outcome:** Các chức năng và dữ liệu của UniSupport được bảo vệ theo quyền truy cập, hạn chế việc truy cập trái phép và hỗ trợ theo dõi các hoạt động quan trọng trong hệ thống.

*Scope Note:* Các chức năng quản lý thông tin người dùng và cập nhật Role bởi Management chỉ được đưa vào phạm vi bàn giao chính thức sau khi được xác nhận trong Project Scope, Master Plan và WBS.

### 4.2. Out of Scope

Trong giai đoạn hiện tại, UniSupport tập trung vào việc thiết kế và xây dựng prototype nhằm minh họa các chức năng và quy trình nghiệp vụ chính. Các nội dung dưới đây chưa thuộc phạm vi triển khai bắt buộc:

- **Production-ready System:** Chưa triển khai hệ thống hoàn chỉnh để vận hành thực tế trên môi trường production.
- **Full System Integration:** Chưa thực hiện tích hợp thực tế với toàn bộ hệ thống hiện có của Aurora University.
- **Real Personal Data:** Không sử dụng dữ liệu cá nhân thật của sinh viên trong prototype và testing. Các hoạt động này sử dụng Simulated Data.
- **Academic Management Replacement:** Không thay thế hệ thống quản lý đào tạo hoặc hệ thống quản lý học vụ hiện có.
- **Tuition Payment:** Không triển khai chức năng thanh toán học phí hoặc xử lý giao dịch tài chính. Các yêu cầu liên quan đến học phí chỉ được quản lý dưới dạng Support Request.
- **Automated Academic Decisions:** Không xây dựng chức năng tự động đưa ra quyết định liên quan đến học vụ hoặc kết quả học tập.
- **University-wide Rollout:** Chưa triển khai hệ thống production trên quy mô toàn trường trong giai đoạn hiện tại.

Các nội dung trên có thể được ghi nhận trong Future Roadmap để xem xét ở những giai đoạn tiếp theo nếu có nhu cầu, nguồn lực và sự phê duyệt phù hợp. Việc đề xuất trong Future Roadmap không đồng nghĩa với cam kết triển khai trong phạm vi dự án hiện tại.

## 5. Project Plan & Timeline

Dự án UniSupport được lập kế hoạch trong thời gian 15 tuần, với bốn Milestones chính. Mỗi Milestone hướng đến việc bàn giao một Product Increment có chức năng cụ thể để Project Sponsor / Simulated Client có thể xem xét và đánh giá.

- **MS-01 – Student Request Submission & Tracking:** Bàn giao chức năng gửi Request và theo dõi Request dành cho Student.
- **MS-02 – Staff Request Classification & Processing:** Bàn giao chức năng phân loại, phân công và xử lý Request dành cho Staff.
- **MS-03 – Request Transfer, Resolution & Feedback:** Bàn giao chức năng chuyển giao, giải quyết, đóng Request và tiếp nhận Feedback.
- **MS-04 – Management Dashboard, Security & Handover:** Bàn giao Management Dashboard, các cơ chế Security and Access và bộ tài liệu hỗ trợ tiếp nhận prototype.

Ngày hoàn thành, dependencies, effort và acceptance criteria của từng Milestone được quản lý trong Master Plan Excel. Mọi thay đổi ảnh hưởng đến Project Baseline phải được đánh giá và phê duyệt theo quy trình Change Control.

## 6. Project Cost & Resource Allocation

### 6.1. Project Constraints

- **Project Duration:** 15 tuần.
- **Delivery Team:** 4 thành viên với trách nhiệm được phân chia rõ ràng.
- **Maximum Effort:** 320 person-hours.
- **Planned Effort:** 304 person-hours.
- **Contingency Reserve:** 16 person-hours.

Nhóm theo dõi Planned Effort và Actual Effort trong suốt quá trình thực hiện. Việc sử dụng Contingency Reserve cần được ghi nhận và không được làm tổng effort vượt quá giới hạn đã được phê duyệt.

### 6.2. Team Structure & Responsibilities

| Role | Main Responsibilities |
|---|---|
| Project Manager (PM) | Quản lý Project Baseline, tiến độ, nguồn lực, rủi ro, thay đổi và điều phối nhóm. |
| Business Analyst (BA) | Phân tích nghiệp vụ, xác định yêu cầu, xây dựng Workflows, PRDs, Acceptance Criteria và hỗ trợ kiểm thử. |
| Front-end Developer (FE) | Thiết kế và xây dựng giao diện prototype cho Student, Staff và Management; đảm bảo Responsive UI và khả năng sử dụng trên máy tính, thiết bị di động. |
| Back-end Developer (BE) | Xây dựng Business Logic, API, Database, Authentication, Role-Based Access Control và xử lý dữ liệu, Request Workflows. |

Các vai trò trên là cơ cấu phân công của Delivery Team. Một thành viên có thể hỗ trợ các hoạt động thuộc vai trò khác khi cần thiết, nhưng mỗi công việc phải có người phụ trách chính rõ ràng.

Tên thành viên đảm nhiệm từng Role được ghi nhận trong Resources Sheet và Team Charter sau khi nhóm xác nhận cơ cấu nhân sự chính thức.

### 6.3. Effort & Cost Estimate

Tổng Planned Effort của các công việc chính là 304 person-hours, tương ứng với chi phí nhân công cơ bản 65.425.000 VNĐ theo Quotation.

Ngoài ra, dự án dành 16 person-hours làm Contingency Reserve để xử lý các vấn đề phát sinh hợp lý. Khoản dự phòng này chưa được tính vào chi phí nhân công cơ bản.

Chi tiết hạng mục công việc, effort, đơn giá và tổng chi phí được trình bày trong Quotation Excel.

Chi phí công cụ và dịch vụ được quản lý riêng, theo danh mục và mức chi phí đã được xem xét, phê duyệt.

Tổng effort của dự án không được vượt quá 320 person-hours nếu chưa có sự phê duyệt chính thức đối với thay đổi Project Baseline.