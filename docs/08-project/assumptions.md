# Project Assumptions

## 1. Purpose

Tài liệu này ghi nhận các giả định được sử dụng để lập kế hoạch, xác định phạm vi và xây dựng Quotation cho dự án UniSupport. Các giả định được xem xét lại nếu điều kiện thực tế, scope, schedule, effort hoặc cost thay đổi.

## 2. Project Assumptions

| ID | Assumption | Reason / Basis | Status |
|---|---|---|---|
| AS-01 | Nhóm đại diện gồm sinh viên và nhân viên sẽ tham gia đánh giá prototype và usability testing. | Kế hoạch review và kiểm thử trong Project Proposal; cần xác nhận khả năng tham gia khi lập lịch. | To Confirm |
| AS-02 | Các chính sách và quy trình hiện hành của trường liên quan đến dịch vụ sinh viên, bảo vệ dữ liệu và quản lý hồ sơ tiếp tục được áp dụng làm bối cảnh tham khảo. | Project Proposal; các chính sách thực tế chưa được cung cấp để xác minh trong dự án mô phỏng. | To Confirm |
| AS-03 | Stakeholders sẽ tham gia các buổi review định kỳ và cung cấp phản hồi trong thời gian dự án. | Project Proposal và kế hoạch review theo milestone. | To Confirm |
| AS-04 | Prototype và testing sử dụng dữ liệu giả lập, đại diện cho quy mô khoảng 3.000 sinh viên; không sử dụng dữ liệu sinh viên thật. | Team planning assumption về dữ liệu và quy mô mô phỏng phục vụ thiết kế prototype và kiểm thử; không dựa trên dữ liệu sinh viên thực tế. | Confirmed for planning |
| AS-05 | Aurora University và Director of Student Services được sử dụng làm Client và Project Sponsor trong bối cảnh mô phỏng của dự án UniSupport. | Simulated client context được sử dụng để xác định stakeholder, trách nhiệm, review và acceptance approach trong project planning. | Confirmed for planning |
| AS-06 | Trong kịch bản handover mô phỏng, Project Sponsor/Director of Student Services hoặc delegate được chỉ định được giả định là Product Decision Owner; BA duy trì backlog và metric evidence, các metric được đề xuất review hằng tháng. | Cần một vai trò nhận feedback, quyết định ưu tiên và xem xét Value Metrics sau handover. Đây là giả định lập kế hoạch, không phải sự ủy quyền thực tế từ Aurora University. | Proposed assumption — subject to simulated client confirmation |

## 3. Pricing Assumption (A-01)

| ID | Assumption | Reason / Basis | Status | Pricing Impact |
|---|---|---|---|---|
| A-01 | Quotation là planning estimate cho phạm vi và effort hiện được lập trong WBS/Master Plan; effort cơ sở 304 person-hours được định giá theo các vai trò PM, BA, FE và BE bằng benchmark lương gross trung vị tham khảo, quy đổi theo 176 giờ/tháng và làm tròn đơn giá đến 5.000 VND/giờ. Mức này không phải báo giá vendor hoặc giá dịch vụ outsource. Contingency Reserve 16 hours được giữ riêng, không nằm trong giá cơ sở; nếu sử dụng, effort phải được phân bổ theo vai trò/công việc, định giá và phê duyệt qua change control. Overhead, thuế, lợi nhuận, chi phí công cụ/dịch vụ trả phí và các chi phí ngoài labour estimate chưa được tính, trừ khi được ghi nhận và phê duyệt riêng. | Quotation.xlsx, sheet `Đơn giá`, `Chi tiết effort`, `Hạng mục` và `Phiên bản`; effort tham chiếu WBS/Master Plan. | Planning assumption — subject to review | Q-01; Q-02; Q-03; Q-04; Q-05; Q-06; Q-07; Q-08 |

## 4. Assumption Management

- Project Manager theo dõi các giả định trong quá trình thực hiện dự án.
- Các giả định cần được xem xét lại khi có thay đổi về scope, requirements, schedule, effort, cost hoặc stakeholder feedback.
- Nếu một giả định không còn đúng, nhóm phải đánh giá ảnh hưởng đến scope, schedule, effort, cost và các deliverables liên quan.
- Những vấn đề chưa được xác nhận phải được ghi nhận trong `open-questions.md`.
- A-01 là nguồn mô tả pricing assumption; sheet `Giả định` trong Quotation chỉ ánh xạ mã A-01 đến các hạng mục Q bị ảnh hưởng, không tạo một nội dung giả định thứ hai.