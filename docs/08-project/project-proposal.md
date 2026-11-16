# UniSupport – Student Support Management System Project
## Project Proposal

### 1. Project Overview

**Project Name:** UniSupport – Student Support Management System Project  
**Project Client:** Aurora University (Simulated Client)  
**Project Sponsor:** Director of Student Services (Simulated Project Sponsor)  
**Project Duration:** 15 Weeks  
**Maximum Project Effort:** 320 Person-Hours

UniSupport là dự án lập kế hoạch và thiết kế một giải pháp quản lý tập trung các yêu cầu hỗ trợ sinh viên tại Aurora University.

Dự án hướng đến việc cải thiện quá trình tiếp nhận, phân công, xử lý và theo dõi yêu cầu. Giải pháp cung cấp các chức năng phù hợp cho sinh viên, nhân viên và ban quản lý, đồng thời xem xét các yêu cầu về bảo mật và quyền truy cập dữ liệu.

Aurora University được giả định có khoảng 3.000 sinh viên. Khi số lượng sinh viên tăng lên, nhà trường cần một phương thức quản lý yêu cầu hỗ trợ rõ ràng và nhất quán hơn.

### 2. Project Background & Problem Statement

#### 2.1 Current Situation

Hiện tại, sinh viên có thể gửi yêu cầu hỗ trợ thông qua nhiều kênh khác nhau, bao gồm email, điện thoại, biểu mẫu trực tuyến, mạng xã hội hoặc trao đổi trực tiếp.

Mỗi phòng ban có thể sử dụng phương thức quản lý riêng. Một số yêu cầu được lưu trong bảng tính, trong khi những yêu cầu khác nằm trong email hoặc tin nhắn cá nhân. Điều này khiến việc quản lý và theo dõi yêu cầu giữa các phòng ban chưa được tập trung.

#### 2.2 Identified Problems

**Student Problems**

- Sinh viên không biết nên liên hệ phòng ban nào.
- Không biết yêu cầu đã được tiếp nhận hay chưa.
- Khó xác định ai đang chịu trách nhiệm xử lý.
- Không thể theo dõi trạng thái yêu cầu một cách thuận tiện.
- Phải liên hệ nhiều lần để hỏi tiến độ.
- Có thể nhận được câu trả lời không thống nhất.
- Có thể phải cung cấp lại thông tin khi yêu cầu được chuyển sang phòng ban khác.

**Staff Problems**

- Yêu cầu được tiếp nhận từ nhiều kênh khác nhau.
- Một số yêu cầu có thể bị bỏ sót hoặc xử lý trùng lặp.
- Khó xác định người chịu trách nhiệm.
- Khó theo dõi lịch sử xử lý.
- Các câu hỏi tương tự phải được trả lời nhiều lần.
- Báo cáo phải được tổng hợp thủ công.

**Management Problems**

- Không nắm chính xác số lượng yêu cầu đang chờ xử lý.
- Khó theo dõi thời gian xử lý trung bình.
- Không xác định được phòng ban đang có khối lượng công việc lớn.
- Thiếu dữ liệu để nhận biết các loại vấn đề phổ biến.
- Khó đánh giá chất lượng dịch vụ hỗ trợ sinh viên.
- Thiếu cơ sở dữ liệu đáng tin cậy để lập kế hoạch nhân sự.

#### 2.3 Problem Statement

Aurora University cần một giải pháp quản lý tập trung để cải thiện khả năng tiếp nhận, phân công, xử lý và theo dõi yêu cầu hỗ trợ sinh viên.

Giải pháp cần giúp sinh viên dễ dàng gửi và theo dõi yêu cầu, hỗ trợ nhân viên phối hợp xử lý công việc, đồng thời cung cấp dữ liệu cần thiết để ban quản lý đánh giá hoạt động hỗ trợ.

### 3. Project Goal & Objectives

#### 3.1 Project Goal

Lập kế hoạch và thiết kế giải pháp UniSupport giúp Aurora University quản lý tập trung quá trình tiếp nhận, phân công, xử lý và theo dõi yêu cầu hỗ trợ sinh viên.

#### 3.2 Project Objectives

Dự án hướng đến các mục tiêu sau:

- Giúp sinh viên gửi yêu cầu hỗ trợ và theo dõi trạng thái dễ dàng hơn.
- Hỗ trợ nhân viên tiếp nhận và xử lý yêu cầu với trách nhiệm rõ ràng.
- Cải thiện khả năng phối hợp giữa các phòng ban.
- Giảm tình trạng yêu cầu bị bỏ sót, xử lý trùng lặp hoặc chậm trễ.
- Cung cấp thông tin để ban quản lý theo dõi khối lượng công việc và chất lượng dịch vụ.
- Bảo đảm dữ liệu sinh viên chỉ được truy cập bởi người có thẩm quyền.

#### 3.3 Expected Outcomes

Các kết quả hướng đến của dự án gồm:

- Ít nhất 90% yêu cầu có người chịu trách nhiệm rõ ràng.
- Ít nhất 90% yêu cầu có trạng thái có thể theo dõi.
- Giảm số lượng yêu cầu bị bỏ sót hoặc xử lý trùng lặp.
- Giảm ít nhất 30% số lần sinh viên phải liên hệ để hỏi tiến độ.
- Hỗ trợ ban quản lý nhận biết các yêu cầu quá hạn.
- Hỗ trợ xác định những vấn đề sinh viên thường gặp.
- Bảo đảm dữ liệu được truy cập theo quyền hạn phù hợp.

Các mục tiêu này sẽ được xem xét và kiểm chứng thông qua prototype, test scenarios, usability testing và dữ liệu giả lập.

### 4. Project Scope

#### 4.1 In Scope

Dự án tập trung vào bốn Modules chính:

**M01 – Student Portal**

Sinh viên có thể gửi yêu cầu hỗ trợ thông qua hệ thống. Khi gửi yêu cầu, sinh viên cung cấp các thông tin cần thiết, lựa chọn loại yêu cầu và đính kèm tài liệu liên quan nếu cần. Hệ thống cung cấp Request ID để sinh viên xác nhận và theo dõi yêu cầu.

Sinh viên cũng có thể xem trạng thái hiện tại, lịch sử cập nhật phù hợp, nhận thông báo khi trạng thái thay đổi và phản hồi nếu kết quả giải quyết chưa đáp ứng vấn đề.

**M02 – Staff Workspace**

Nhân viên có thể xem các yêu cầu được phân công, cập nhật trạng thái và ghi nhận hoạt động xử lý. Trong quá trình làm việc, nhân viên có thể yêu cầu sinh viên bổ sung thông tin hoặc chuyển yêu cầu đến đơn vị khác khi cần thiết.

Module này hỗ trợ việc phân công trách nhiệm và theo dõi quá trình xử lý yêu cầu.

**M03 – Management Dashboard**

Ban quản lý có thể theo dõi tình hình xử lý yêu cầu thông qua các thông tin và báo cáo tổng hợp.

Các nội dung theo dõi bao gồm số lượng yêu cầu mới, số lượng yêu cầu đang xử lý, yêu cầu quá hạn, thời gian xử lý trung bình, loại yêu cầu phổ biến, khối lượng công việc của từng phòng ban và mức độ hài lòng của sinh viên.

**M04 – Security and Access**

Hệ thống xem xét các yêu cầu bảo mật và kiểm soát quyền truy cập, bao gồm xác thực người dùng, phân quyền theo vai trò, giới hạn quyền truy cập dữ liệu sinh viên và bảo vệ tài liệu đính kèm.

Module này cũng xem xét việc ghi nhận lịch sử truy cập và thay đổi, thời gian lưu trữ dữ liệu và xử lý dữ liệu nhạy cảm.

Lưu ý: Phạm vi Role Administration, tức chức năng cho phép quản lý tự tạo hoặc thay đổi Role, chưa được xác nhận là chức năng bàn giao chính thức. Vì vậy, chức năng này không được xem là cam kết In Scope ở thời điểm hiện tại.

#### 4.2 Out of Scope & Future Considerations

Trong giai đoạn hiện tại, dự án ưu tiên xây dựng prototype và các tài liệu cần thiết để kiểm chứng giải pháp. Một số nội dung có thể được xem xét trong future roadmap khi có đủ nguồn lực và sự phê duyệt phù hợp:

- Hoàn thiện sản phẩm production để triển khai chính thức.
- Tích hợp thực tế với toàn bộ hệ thống hiện có của trường.
- Sử dụng dữ liệu cá nhân thật.
- Thay thế hệ thống quản lý đào tạo.
- Xử lý thanh toán học phí.
- Tự động đưa ra quyết định học vụ.
- Triển khai trên quy mô toàn trường.

Các nội dung trên không phải trọng tâm của phạm vi hiện tại và không được làm ảnh hưởng đến tính khả thi của các chức năng chính.

### 5. Project Plan & Timeline

#### 5.1 Project Duration

Dự án được lập kế hoạch trong 15 tuần. Việc phát triển và bàn giao được tổ chức theo bốn Product Increment Milestones nhằm cung cấp từng phần sản phẩm có thể xem xét và dùng thử.

#### 5.2 Product Increment Milestones

| Milestone | Target Completion |
|---|---|
| MS-01 | 15 January 2027 |
| MS-02 | 29 January 2027 |
| MS-03 | 12 February 2027 |
| MS-04 | 26 February 2027 |

Mỗi Milestone đại diện cho một mốc bàn giao Product Increment theo Product Roadmap và Master Plan.

Các buổi đánh giá học phần như Intermediate Project Review hoặc Final Presentation không được sử dụng thay thế cho Product Increment Milestones.

#### 5.3 Project Resources

Dự án phân bổ nguồn lực theo bốn vai trò chính:

| Role | Planned Effort |
|---|---:|
| Project Manager (PM) | 68 hours |
| Business Analyst (BA) | 78 hours |
| Front-end Developer (FE) | 79 hours |
| Back-end Developer (BE) | 79 hours |
| **Total** | **304 hours** |

Mỗi vai trò chịu trách nhiệm đối với các công việc phù hợp với chuyên môn. Nhóm sẽ theo dõi planned effort và actual effort để kiểm soát tiến độ và mức độ sử dụng nguồn lực.

### 6. Project Cost & Resource Allocation

#### 6.1 Planned Effort

Tổng effort được lập kế hoạch là 304 person-hours.

Dự án dành thêm 16 person-hours làm Contingency Reserve để xử lý các tình huống phát sinh trong quá trình thực hiện.

| Cost/Effort Item | Amount |
|---|---:|
| Planned Effort | 304 person-hours |
| Contingency Reserve | 16 person-hours |
| **Maximum Project Effort** | **320 person-hours** |

Tổng effort bao gồm cả phần dự phòng không được vượt quá giới hạn 320 person-hours.

#### 6.2 Estimated Project Cost

Theo Quotation hiện tại, tổng chi phí nhân công dự kiến là:

**65,425,000 VND**

Chi phí này được xây dựng dựa trên phân bổ nguồn lực và effort của các vai trò trong dự án.

Các khoản chi phí công cụ hoặc dịch vụ trả phí, nếu phát sinh, cần được giải thích, phân bổ và phê duyệt trước khi đưa vào ngân sách chính thức.

### 7. Project Risks

Dự án có thể gặp một số rủi ro ảnh hưởng đến phạm vi, tiến độ, chất lượng và khả năng bàn giao.

| Risk | Potential Impact | Proposed Response |
|---|---|---|
| Requirement Changes | Thay đổi yêu cầu có thể ảnh hưởng đến phạm vi và effort đã lập kế hoạch. | Theo dõi yêu cầu thay đổi và đánh giá ảnh hưởng trước khi chấp thuận. |
| Conflicting Stakeholder Expectations | Các bên liên quan có thể đưa ra yêu cầu khác nhau hoặc mâu thuẫn. | Ghi nhận vấn đề, làm rõ yêu cầu và xin xác nhận trước khi triển khai. |
| Schedule and Resource Constraints | Thiếu nguồn lực hoặc phân bổ effort không hợp lý có thể làm chậm tiến độ. | Theo dõi tiến độ và actual effort thường xuyên, ưu tiên các công việc thuộc phạm vi chính. |
| Quality Issues | Deliverable không đáp ứng quality criteria có thể bị khách hàng từ chối. | Thực hiện review, testing và kiểm tra deliverable trước khi bàn giao. |
| Data Security and Privacy | Dữ liệu sinh viên có thể bị truy cập không phù hợp nếu quyền truy cập không được kiểm soát. | Sử dụng dữ liệu giả lập và xem xét xác thực, phân quyền, bảo vệ tài liệu và lịch sử truy cập. |
| Incomplete Project Handover | Nhóm tiếp nhận có thể gặp khó khăn nếu tài liệu bàn giao không đầy đủ. | Duy trì tài liệu dự án, liên kết requirements, testing và hướng dẫn bàn giao rõ ràng. |

Các rủi ro sẽ được theo dõi chi tiết trong Risk Register, bao gồm mức độ ảnh hưởng, Risk Owner, preventive actions và response actions.

### 8. Project Constraints & Assumptions

#### 8.1 Project Constraints

- Thời gian thực hiện dự án là 15 tuần.
- Tổng effort tối đa là 320 person-hours.
- Mọi hoạt động cần có effort estimate.
- Nhóm cần theo dõi planned effort và actual effort.
- Prototype và testing sử dụng dữ liệu giả lập.
- Giải pháp cần xem xét khả năng sử dụng trên thiết bị di động và máy tính.
- Giải pháp cần xem xét hỗ trợ tiếng Việt và tiếng Anh.
- Người dùng có thể có mức độ thành thạo công nghệ khác nhau.
- Deliverables cần đáp ứng quality criteria trước khi bàn giao.

#### 8.2 Assumptions

- Aurora University là khách hàng giả lập của dự án.
- Director of Student Services là Project Sponsor giả lập.
- Dữ liệu được sử dụng trong prototype và testing là dữ liệu giả lập.
- Các chức năng được triển khai dựa trên phạm vi và yêu cầu đã được thống nhất.
- Những thay đổi lớn về phạm vi cần được xem xét và phê duyệt trước khi thực hiện.

### 9. Conclusion

UniSupport hướng đến việc cải thiện hoạt động quản lý yêu cầu hỗ trợ sinh viên tại Aurora University thông qua một giải pháp tập trung, có khả năng theo dõi và hỗ trợ phối hợp giữa các bên liên quan.

Với phạm vi gồm bốn Modules, kế hoạch triển khai theo bốn Product Increment Milestones và giới hạn tối đa 320 person-hours, dự án tập trung vào việc xây dựng một giải pháp khả thi, có thể kiểm chứng bằng prototype và có đầy đủ tài liệu phục vụ việc tiếp nhận, đánh giá và bàn giao.

Dự án ưu tiên hoàn thành các chức năng nghiệp vụ cốt lõi trước khi xem xét các khả năng mở rộng trong tương lai.