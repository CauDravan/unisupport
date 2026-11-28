# Risk Register

## 1. Purpose

Risk Register được sử dụng để nhận diện, đánh giá và theo dõi những rủi ro có thể ảnh hưởng đến quá trình thực hiện dự án UniSupport.

Tài liệu giúp nhóm chủ động chuẩn bị các biện pháp phòng ngừa và ứng phó, hạn chế ảnh hưởng của rủi ro đến project scope, schedule, effort và chất lượng deliverables.

Risk Register áp dụng cho toàn bộ thời gian thực hiện dự án 15 tuần.

## 2. Risk Assessment Method

Các rủi ro được đánh giá dựa trên hai tiêu chí:

| Criteria | Description |
|---|---|
| Probability | Khả năng rủi ro có thể xảy ra. |
| Impact | Mức độ ảnh hưởng của rủi ro đến dự án nếu xảy ra. |

**Rating Scale:**

| Level | Probability | Impact |
|---|---|---|
| Low | Khả năng xảy ra thấp | Ảnh hưởng nhỏ, có thể xử lý trong phạm vi công việc hiện tại. |
| Medium | Có khả năng xảy ra | Có thể ảnh hưởng đến tiến độ hoặc chất lượng một số deliverables. |
| High | Khả năng xảy ra cao | Có thể ảnh hưởng đáng kể đến project scope, schedule, effort hoặc kết quả dự án. |

Mức độ Rủi ro Tổng thể được xác định bằng cách kết hợp các chỉ số Đánh giá Xác suất và Mức độ Ảnh hưởng theo ma trận dưới đây:

| Probability / Impact | Low Impact | Medium Impact | High Impact |
|---|---|---|---|
| **Low Probability** | Low | Low | Medium |
| **Medium Probability** | Low | Medium | High |
| **High Probability** | Medium | High | High |

**Risk Level** được xác định dựa trên sự kết hợp giữa Probability và Impact. Những rủi ro có mức đánh giá cao cần được ưu tiên theo dõi và xử lý.

## 3. Risk Register

| ID | Risk Description | Probability | Impact | Risk Level | Risk Owner | Status |
|---|---|---|---|---|---|
| R-01 | Scope Creep – Các bên liên quan yêu cầu bổ sung hoặc thay đổi chức năng sau khi phạm vi ban đầu đã được thống nhất. | High | High | High | PM | Open |
| R-02 | Resource Overload – Thành viên gặp quá tải hoặc không thể hoàn thành công việc theo kế hoạch. | Medium | High | High | PM | Open |
| R-03 | Conflicting Stakeholder Requirements – Các bên liên quan đưa ra những yêu cầu khác nhau hoặc mâu thuẫn. | Medium | Medium | Medium | BA | Open |
| R-04 | Design and Testing Delays – Hoạt động thiết kế hoặc kiểm thử bị chậm, làm giảm thời gian dành cho việc hoàn thiện prototype. | Medium | High | High | PM | Open |
| R-05 | Data Security and Unauthorized Access – Dữ liệu bị sử dụng không phù hợp hoặc người dùng có thể truy cập thông tin ngoài quyền hạn. | Medium | High | High | BE | Open |
| R-06 | Prototype Quality Issues – Prototype không đáp ứng đầy đủ các yêu cầu chức năng hoặc acceptance criteria đã thống nhất. | Medium | High | High | BA | Open |
| R-07 | Incomplete Documentation and Handover – Tài liệu hoặc hướng dẫn bàn giao không đầy đủ, khiến nhóm tiếp nhận khó hiểu và tiếp tục phát triển hệ thống. | Medium | Medium | Medium | PM | Open |

### 3.1 Risk ID Convention

Mỗi rủi ro được gán một mã định danh duy nhất theo định dạng `R-01`, `R-02`, `R-03`... Mã rủi ro được sử dụng thống nhất trong Risk Register để theo dõi, trao đổi, cập nhật và quản lý các rủi ro xuyên suốt dự án. Mã đã được gán không thay đổi nhằm đảm bảo khả năng truy vết.

### 3.2 Risk Status

Trạng thái được sử dụng để theo dõi tình hình quản lý từng rủi ro:

- **Open:** Rủi ro đã được xác định và đang được theo dõi. Các biện pháp phòng ngừa hoặc ứng phó có thể chưa hoàn tất.
- **Mitigated:** Các biện pháp giảm thiểu đã được thực hiện nhằm giảm khả năng xảy ra hoặc mức độ ảnh hưởng của rủi ro. Rủi ro vẫn được theo dõi khi cần thiết.
- **Closed:** Rủi ro không còn cần tiếp tục theo dõi hoặc xử lý sau khi được xem xét và xác nhận.

Project Manager phối hợp với Risk Owner cập nhật trạng thái khi có thay đổi liên quan hoặc trong quá trình review Risk Register.

## 4. Risk Response Strategy

| ID | Mitigation / Preventive Actions | Contingency / Response |
|---|---|---|
| R-01 | Ghi nhận và đánh giá các yêu cầu thay đổi trước khi thực hiện. Xác nhận project scope và kiểm soát các thay đổi có thể làm tăng effort. | Ưu tiên các chức năng cốt lõi, điều chỉnh hoặc hoãn những yêu cầu không cần thiết để bảo đảm giới hạn 320 person-hours. | Open |
| R-02 | Phân công công việc rõ ràng theo vai trò, theo dõi planned effort và actual effort thường xuyên. | Điều chỉnh phân công, hỗ trợ thành viên gặp khó khăn và ưu tiên các công việc ảnh hưởng trực tiếp đến milestone. | Open |
| R-03 | Tổ chức review định kỳ và xác nhận các yêu cầu quan trọng với stakeholders trước khi triển khai. | Đưa ra các phương án thay thế và thống nhất quyết định cuối cùng trước khi tiếp tục thực hiện. | Open |
| R-04 | Theo dõi tiến độ thiết kế và kiểm thử theo Project Schedule, phân bổ thời gian dự phòng và ưu tiên các chức năng chính để hạn chế ảnh hưởng đến các milestone. | Điều chỉnh thứ tự ưu tiên công việc, giảm phạm vi các chức năng phụ và tập trung hoàn thành những luồng nghiệp vụ quan trọng để bảo đảm các milestone chính. | Open |
| R-05 | Sử dụng dữ liệu mô phỏng, áp dụng authentication và role-based access control trong prototype. | Kiểm tra và khắc phục quyền truy cập không phù hợp, điều chỉnh cơ chế phân quyền và dữ liệu liên quan. | Open |
| R-06 | Xây dựng Acceptance Criteria rõ ràng và thực hiện kiểm thử các chức năng chính trong quá trình phát triển để phát hiện lỗi sớm. | Ghi nhận các defect, ưu tiên sửa lỗi ảnh hưởng đến các luồng nghiệp vụ cốt lõi và kiểm tra lại trước khi trình diễn prototype. | Open |
| R-07 | Chuẩn hóa cấu trúc tài liệu, cập nhật nội dung theo quá trình thực hiện và chuẩn bị hướng dẫn sử dụng, thiết lập hệ thống. | Bổ sung tài liệu còn thiếu và thực hiện handover review trước khi kết thúc dự án. | Open |

## 5. Risk Monitoring

Project Manager chịu trách nhiệm theo dõi Risk Register và phối hợp với các thành viên liên quan để cập nhật tình trạng rủi ro.

- Risk Register được xem xét định kỳ trong các buổi project review.
- Khi xuất hiện rủi ro mới, nhóm cần ghi nhận và đánh giá trước khi quyết định biện pháp xử lý.
- Khi Probability hoặc Impact thay đổi, Risk Level cần được đánh giá lại.
- Các rủi ro có thể ảnh hưởng đến project scope, schedule hoặc giới hạn 320 person-hours cần được thông báo và thảo luận trong nhóm.
- Các rủi ro có thể ảnh hưởng đến Phạm vi Dự án, Các cột mốc quan trọng, Tổng thời gian 15 tuần của dự án, hoặc Giới hạn nỗ lực tối đa 320 giờ-người phải được cả nhóm báo cáo, đánh giá và thảo luận để đưa ra các biện pháp ứng phó phù hợp.

Risk Register có thể được cập nhật trong suốt vòng đời dự án nhằm phản ánh tình trạng thực tế và những thay đổi đã được thống nhất. Status `Open` ở bảng đăng ký chỉ thể hiện rủi ro đang được theo dõi; PM/Risk Owner cần cập nhật status sau khi response được thực hiện hoặc rủi ro không còn áp dụng. Tần suất review được thực hiện trong project review và khi có trigger ảnh hưởng đến baseline.
