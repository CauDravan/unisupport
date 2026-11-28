# Success Metrics

## 1. Purpose

Tài liệu này xác định cách đánh giá UniSupport có đáp ứng các mục tiêu sản phẩm và các outcomes được xác định trong bộ tài liệu planning hiện tại hay không.

Các kết quả đo trên prototype chỉ phản ánh khả năng minh họa và kiểm thử trong môi trường mô phỏng. Không được diễn giải thành số liệu cải thiện thực tế của Aurora University khi chưa có dữ liệu vận hành thực tế và phương pháp đo được Client xác nhận.

## 2. Measurement Principles

- Mỗi Metric phải có định nghĩa, công thức hoặc cách kiểm tra, nguồn dữ liệu và điều kiện đo rõ ràng.
- Dùng Simulated Data; không sử dụng dữ liệu cá nhân thật của sinh viên.
- Ghi rõ thời điểm đo, phiên bản prototype, bộ dữ liệu, số lượng Request và kịch bản kiểm thử.
- Không báo cáo một mục tiêu là đạt nếu chưa thực hiện phép đo hoặc chưa có bằng chứng.
- Nếu thiếu baseline hoặc dữ liệu phù hợp, ghi nhận là **Not Measured / Requires Baseline**, không tự ước lượng kết quả.
- Các mục tiêu định lượng hiện được sử dụng làm planning targets cho prototype; phương pháp kiểm chứng được xác định trong Test Scenarios và các tài liệu kiểm thử liên quan.

## 3. Product Success Metrics

| ID | Success Metric | Target | Measurement Method | Evidence |
|---|---|---|---|---|
| VM-01 | Request Assignment Coverage | At least 90% of Requests have a clearly identified responsible owner. | `(Số Request có Department hoặc Staff chịu trách nhiệm rõ ràng / Tổng số Request được ghi nhận) × 100%`. Kiểm tra dữ liệu Request và Assignment trong bộ dữ liệu giả lập. | Request records, Assignment data, Test Scenarios liên quan đến Classification & Assignment. |
| VM-02 | Request Tracking Coverage | At least 90% of Requests have a recorded and trackable Status. | `(Số Request có Status hợp lệ và có thể tra cứu / Tổng số Request được ghi nhận) × 100%`. Đối chiếu Status với danh mục trong `request-status.md`. | Request records, Student Portal, Status history và Test Scenarios. |
| VM-03 | Student Progress Inquiry Reduction | At least 30% reduction in the number of Student contacts asking for request progress. | So sánh số lần liên hệ hỏi tiến độ trong hai giai đoạn có thể so sánh: trước và sau khi sử dụng quy trình tracking. Công thức: `((Baseline contacts − Post-use contacts) / Baseline contacts) × 100%`. Cần có baseline và cùng cách ghi nhận ở cả hai giai đoạn. | Baseline contact log và post-use contact log. Nếu chỉ có prototype/simulated data, kết quả là mô phỏng, không phải mức giảm thực tế. |
| VM-04 | Overdue Request Visibility | Management can identify overdue Requests. | Kiểm tra Management Dashboard có hiển thị Request được xác định quá hạn theo thời gian xử lý mục tiêu đã cấu hình. Không tự đặt SLA hoặc ngưỡng quá hạn mới. | Dashboard demonstration, cấu hình thời gian xử lý mục tiêu và test data. |
| VM-05 | Common Issue Identification | Management can identify common student issues. | Kiểm tra báo cáo tổng hợp Request theo Request Type, số lượng và tỷ lệ; đối chiếu với dữ liệu nguồn. | Management reports và Simulated Request dataset. |
| VM-06 | Authorized Data Access | Data is accessible only to authorized users. | Thực hiện kiểm thử Role Permission Matrix cho Student, Staff và Management; các trường hợp truy cập trái quyền phải bị từ chối. | Access-control Test Scenarios, test accounts và kết quả kiểm thử. |
| VM-07 | Student Satisfaction Monitoring | Management can review Student Feedback and satisfaction information. | Các chỉ số không có target số cụ thể trong planning baseline được đánh giá theo khả năng chức năng và bằng chứng kiểm thử; không tự bổ sung ngưỡng phần trăm. | Feedback records, WF-07 và Management Dashboard/report. |

## 4. Measurement Procedure

1. **Prepare Dataset:** Chuẩn bị bộ Simulated Data có các Request Type, Status, Assignment và Feedback cần thiết cho từng phép đo.
2. **Prepare Scenarios:** Chọn Test Scenarios và workflow tương ứng; xác định trước điều kiện đầu vào và kết quả mong đợi.
3. **Execute:** Thực hiện prototype demonstration hoặc test theo cùng một bộ điều kiện đã xác định.
4. **Collect Evidence:** Ghi lại số liệu nguồn, kết quả test, ảnh chụp hoặc log phù hợp. Không chỉ ghi kết luận đạt/không đạt.
5. **Calculate and Review:** Tính các tỷ lệ theo công thức trong bảng; kiểm tra lại mẫu số, dữ liệu thiếu và các trường hợp ngoại lệ.
6. **Report:** Ghi kết quả, ngày đo, phiên bản prototype, người thực hiện, giới hạn đo và trạng thái: Met, Not Met, Not Measured hoặc Requires Baseline.

## 5. Measurement Record Template

| Field | Required Information |
|---|---|
| Metric ID | VM-01 đến VM-07. |
| Measurement Date | Ngày thực hiện phép đo. |
| Prototype Version | Phiên bản hoặc commit được kiểm tra. |
| Dataset | Tên/phiên bản bộ Simulated Data và số lượng bản ghi. |
| Scenario / Method | Test Scenario, demonstration hoặc usability method được sử dụng. |
| Observed Result | Số liệu thực tế thu được trong lần đo. |
| Target | Mục tiêu tương ứng trong bảng Success Metrics. |
| Status | Met / Not Met / Not Measured / Requires Baseline. |
| Evidence | Liên kết test result, log, ảnh chụp hoặc file dữ liệu. |
| Limitation / Note | Giới hạn và giả định ảnh hưởng đến kết quả. |

## 6. Metric Ownership and Review Cycle

Đối với quá trình bàn giao mô phỏng, mô hình sở hữu tạm thời được đề xuất là:

| Metrics | Interim tracking owner during project / handover preparation | Proposed post-handover owner (assumption, not confirmed by Aurora University) | Review cycle |
|---|---|---|---|
| VM-01, VM-02 | BA; PM tập hợp các bằng chứng | Product Owner mảng Dịch vụ Sinh viên hoặc người được ủy quyền | Hàng tháng |
| VM-03 | BA; PM đảm bảo các thông số cơ sở/phương pháp luận được ghi lại bằng văn bản | Chủ sở hữu quy trình dịch vụ mảng Dịch vụ Sinh viên hoặc người được ủy quyền | Hàng tháng (chỉ áp dụng khi có dữ liệu tương đương) |
| VM-04, VM-05 | BA (kèm bằng chứng kiểm thử bảng điều khiển/dashboard) | Product Owner thuộc Dịch vụ Sinh viên hoặc người được ủy quyền | Hàng tháng |
| VM-06 | BE (với sự xác nhận từ BA) | Vai trò phụ trách CNTT/bảo mật do Nhà trường chỉ định | Hàng tháng hoặc sau khi có thay đổi về kiểm soát truy cập |
| VM-07 | BA | Product Owner phản hồi/dịch vụ thuộc Dịch vụ Sinh viên hoặc người được ủy quyền | Hàng tháng |

Trong suốt dự án, BA duy trì định nghĩa các chỉ số và bằng chứng; PM đảm bảo gói bàn giao ghi lại các chủ sở hữu được đề xuất và các xác nhận còn thiếu. Nhà tài trợ/Giám đốc Dịch vụ Sinh viên giả định sẽ đưa ra các quyết định ưu tiên sản phẩm cho đến khi một đại diện của trường đại học được chỉ định chính thức. Giả định này không khẳng định sự ủy quyền thực sự của trường đại học.

## 7. Baseline and Open Decisions

- **VM-03:** Cần baseline về số lần Student liên hệ hỏi tiến độ và cách ghi nhận thống nhất trước/sau. Client giả định chưa cung cấp dữ liệu vận hành thực tế; prototype chỉ có thể minh họa phép tính bằng dữ liệu giả lập.
- **VM-04:** Cần thời gian xử lý mục tiêu hoặc quy tắc xác định quá hạn được cấu hình. Giá trị cụ thể chưa được nguồn dự án xác nhận; không tự đặt SLA.
- **VM-01 và VM-02:** Cần thống nhất bộ Request dùng làm mẫu số, bao gồm cách xử lý Request bị hủy hoặc dữ liệu chưa hoàn chỉnh nếu các trường hợp này xuất hiện trong prototype.
- **VM-07:** Chưa có mục tiêu định lượng về mức độ hài lòng được Client xác nhận; chỉ đánh giá khả năng thu thập và xem Feedback.
- Các chủ sở hữu chỉ số được đề xuất và chu kỳ đánh giá hàng tháng là những giả định lập kế hoạch phục vụ cho quá trình bàn giao mô phỏng; Đại học Aurora cần xác nhận hoặc thay thế các thông tin này trước khi đưa vào sử dụng thực tế.

## 8. Scope Limitations

- Các tỷ lệ từ Simulated Data không đại diện cho kết quả vận hành tại Aurora University.
- Mục tiêu giảm 30% số lần liên hệ hỏi tiến độ chỉ có thể được xác minh thực tế khi có baseline và dữ liệu sau triển khai phù hợp.
- Prototype demonstration chứng minh chức năng có thể thực hiện; không tự chứng minh mức cải thiện quy mô toàn trường.
- Các chỉ số không có target số cụ thể trong Project Requirements hoặc được Client xác nhận sẽ được đánh giá theo khả năng chức năng và bằng chứng kiểm thử; không tự bổ sung ngưỡng phần trăm.

## 9. Related Documents

- [Product Goals](../01-product/product-goals.md)
- [Product Backlog](../01-product/product-backlog.md)
- [Product Scope](../01-product/product-scope.md)
- [Non-Functional Requirements](../05-requirements/non-functional-requirements.md)
- [Test Scenarios](../06-acceptance/test-scenarios.md)
- [Traceability Matrix](../06-acceptance/traceability-matrix.md)
- [Quality Plan](../09-quality/quality-plan.md)
- [Feedback Process](./feedback-process.md)
