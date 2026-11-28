# Ghi chú rà soát và chỉnh sửa theo Feedback Round 3

**Ngày rà soát:** 28/11/2026  
**Trạng thái:** Bản chỉnh sửa phục vụ rà soát nội bộ; chưa phải bản đã được nhóm hoặc Sponsor (mô phỏng) phê duyệt.

## 1. Các chỉnh sửa đã thực hiện (cần nhóm xác nhận)

- **V4-01 – Scope và Traceability:** Đã cập nhật Product Scope, Functional Requirements, WF-08, Test Scenarios và Traceability Matrix: Login (FR-SEC-03) được giữ trong baseline, MS-01; Request Reopening (WF-08, BR-06–BR-09, AC-07–AC-10, TS-083–TS-086) được tách và đánh dấu Proposed, excluded from baseline. Câu hỏi scope được theo dõi bằng OQ-12. Cần review chéo Quotation/WBS/GitHub để xác nhận không tính reopening vào effort cam kết.
- **V4-02 – WBS và tiến độ:** Đã đề xuất điều chỉnh một số tuần thực hiện task để giảm chồng lấn và cập nhật mục tiêu MS-04 sang 26/02/2027. Lịch vẫn cần kiểm tra thủ công, tính lại công thức Excel và đối chiếu quan hệ phụ thuộc.
- **V4-03 – Project Proposal:** Đã điều chỉnh một số nội dung trong Markdown và bản tham chiếu ở thư mục `sent/` để mô tả nhất quán hơn kết quả dự kiến (prototype có thể chạy, dùng thử cùng các tài liệu planning/design). Word được cập nhật ở những nội dung khớp. PDF chưa được xuất lại; thư mục `sent/` chưa phải bằng chứng đã gửi hoặc được phê duyệt.
- **V4-04 – Issue Templates:** Đã khôi phục các template và Pull Request template từ commit trong repository. Chỉ kiểm tra tĩnh tại repository; chưa kiểm tra giao diện tạo Issue trên GitHub.
- **V4-05 – GitHub Issues:** Chưa hoàn tất việc phân nhóm Issue theo Milestone, người phụ trách và ngày hạn trong các trường native của GitHub. Cần kiểm tra các Issue #8, #22, #28, #29, #30 và các Issue liên quan.
- **V4-06 – Governance:** Đã bổ sung ngưỡng escalation đề xuất và lưu ý hạn chế của dữ liệu metrics khi các trường/labels trên GitHub chưa được xác minh. Các ngưỡng chưa được Sponsor xác nhận.
- **V4-07 – Risk Register:** Đã chỉnh định dạng bảng, tách Owner và Status, đồng nhất mã rủi ro theo dạng R-01 đến R-07.
- **V4-08 – Acceptance Criteria:** Đã bổ sung AC cho trường hợp Request History trống và thay đổi Role khi phiên đăng nhập đang hoạt động; thêm TS-110/111 và Traceability. Cần nhóm xác nhận phạm vi, tính khả thi và mapping milestone.
- **V4-09 – Test Scenarios:** Đã thêm cột Critical/Core để nhóm xác định kịch bản quan trọng theo từng milestone. Việc phân loại chưa hoàn tất và chưa thể xem release gate là đã chốt.
- **V4-10 – Terminology và nguồn căn cứ:** Đã chỉnh một số cách diễn đạt liên quan đến đề bài môn học trong các tài liệu được rà soát. Cần tìm kiếm toàn repository và xác định cách dùng phù hợp cho tài liệu nội bộ so với tài liệu hướng tới Client.

## 2. Các việc còn cần thực hiện

1. Xác nhận OQ-12 về Request Reopening với nhóm/Sponsor mô phỏng; nếu thay đổi phạm vi, cập nhật đồng bộ Proposal, Quotation, WBS/effort và mapping Issue.
2. Rà soát GitHub Issues #1–#35, đặc biệt #8, #22, #28, #29, #30; chia task nếu task đang trải qua nhiều milestone, đặt milestone đúng và điền Assignee/Due date vào trường tương ứng.
3. Kiểm tra cả bốn Issue templates trên giao diện New Issue của GitHub; xác minh labels và cấu hình template.
4. Nhóm phân loại Critical/Core cho từng Test Scenario theo milestone, sau đó xác nhận các release gate trong Quality Plan.
5. Mở Master Plan Excel bằng Excel/LibreOffice để tính lại công thức; kiểm tra dependency, tuần thực hiện, ngày milestone và effort.
6. Đồng bộ Proposal Markdown, DOCX và PDF. Chỉ lưu trong `sent/` bản thực sự đã gửi hoặc ghi rõ đó là bản tham chiếu chưa gửi.
7. Xác nhận các AC mới dựa trên Workflow và ý định stakeholder; đặc biệt là hành vi khi Role thay đổi trong phiên đang hoạt động.
8. Xác nhận các ngưỡng escalation đề xuất: task trễ ít nhất 1 ngày làm việc; dự báo milestone trễ ít nhất 2 ngày lịch; hoặc đã sử dụng 50% contingency khi milestone vẫn có nguy cơ. Đây là đề xuất nội bộ, chưa phải cam kết đã được Sponsor chấp thuận.

## 3. Phạm vi file đã chỉnh

Các file có thay đổi nằm ở Product Scope, WF-08, Functional/Non-Functional Requirements, Acceptance Criteria/Test Scenarios/Traceability, Master Plan (MD/XLSX), Proposal (MD/DOCX và bản tham chiếu), Risk Register, RACI, Success Metrics và Governance. Các file/Issue trên GitHub và PDF Proposal chưa được cập nhật trực tiếp.

## 4. V4-01 Repair Record

- Product Scope: giữ FR-SEC-03 trong baseline; Request Reopening được nêu rõ là Proposed, ngoài baseline.
- Functional Requirements: BR-06–BR-09 và AC-07–AC-10 được tách khỏi yêu cầu baseline FR-STU-03 sang phần Proposed Feature.
- WF-08: giữ workflow draft; related references được cập nhật để chỉ rõ Proposed Rules.
- Test Scenarios: TS-083–TS-086 vẫn được giữ, nhưng không thuộc release gate hoặc baseline acceptance.
- Traceability Matrix: tách mapping reopening sang Proposed Feature Traceability.
- Open Questions: thêm OQ-12; không dùng Q-01 (Quotation code) làm mã Open Question.
- Chưa chỉnh Master Plan, Quotation hoặc GitHub native issues trong repair này; các phần đó cần kiểm tra ở audit tiếp theo.
