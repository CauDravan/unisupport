# Non-Functional Requirements

Tài liệu này xác định các tiêu chí chất lượng mà UniSupport cần đáp ứng trong phạm vi prototype. Mỗi yêu cầu có mã định danh, ngưỡng đánh giá và phương pháp kiểm thử để nhóm có thể xác minh bằng dữ liệu mô phỏng.

> **Lưu ý về ngưỡng đo:** Đề bài chưa quy định các con số về thời gian phản hồi, tải đồng thời và usability. Vì vậy, các ngưỡng có ghi **Proposed baseline** là mức đề xuất để kiểm thử prototype, không phải cam kết production hoặc số liệu đã được Aurora University phê duyệt. Nhóm cần xác nhận các ngưỡng này với Project Sponsor trước khi chốt baseline nghiệm thu. Những nội dung chưa có chính sách nguồn được ghi rõ là cần xác nhận, không tự đặt giá trị.

## 1. Performance

| ID | Yêu cầu | Ngưỡng đo đề xuất | Cách đo | Áp dụng cho |
| --- | --- | --- | --- | --- |
| `NFR-PERF-01` | Các thao tác chính gồm mở Request Form, gửi Request và xem Request Detail phải phản hồi trong thời gian phù hợp. | **Proposed baseline:** ít nhất 95% lượt thao tác hoàn tất trong không quá 3 giây; kiểm thử với 10 phiên người dùng đồng thời và bộ dữ liệu 1.000 Request giả lập. | Chạy lặp lại từng thao tác trong cùng môi trường kiểm thử, sử dụng bộ dữ liệu 1.000 Request giả lập và tối đa 10 phiên người dùng đồng thời. Ghi nhận thời gian từ lúc người dùng thực hiện thao tác đến khi hệ thống hiển thị kết quả hoàn chỉnh. Tính tỷ lệ lượt thao tác hoàn tất trong ngưỡng thời gian quy định. | M01, M02 |
| `NFR-PERF-02` | Management Dashboard và các báo cáo tổng quan phải tải dữ liệu trong thời gian phù hợp. | **Proposed baseline:** ít nhất 95% lượt tải Dashboard hoàn tất trong không quá 5 giây với cùng bộ dữ liệu 1.000 Request giả lập và 10 phiên đồng thời. | Chạy lặp lại thao tác mở Dashboard và từng báo cáo trong cùng môi trường kiểm thử. Ghi nhận thời gian từ lúc Management truy cập chức năng đến khi dữ liệu và biểu đồ cần thiết hiển thị hoàn chỉnh. Tính tỷ lệ lượt tải đạt ngưỡng thời gian quy định. | M03 |
| `NFR-PERF-03` | Hệ thống phải truy vấn, lọc và tổng hợp chính xác bộ dữ liệu giả lập đã thống nhất. | 100% bản ghi trong bộ dữ liệu kiểm thử được truy vấn, lọc và tổng hợp đúng theo dữ liệu nguồn. Quy mô bộ dữ liệu nghiệm thu chính thức cần được nhóm và Sponsor xác nhận. | Đối chiếu kết quả truy vấn, bộ lọc, số liệu Dashboard và báo cáo với dữ liệu nguồn đã chuẩn bị. Kiểm tra các trường hợp có dữ liệu, không có dữ liệu và dữ liệu thuộc nhiều Status hoặc Request Type khác nhau. | M01, M02, M03 |

## 2. Usability

| ID | Yêu cầu | Ngưỡng đo | Cách đo | Áp dụng cho |
| --- | --- | --- | --- | --- |
| `NFR-USE-01` | Student có thể hoàn thành các tác vụ cốt lõi: gửi Request và xem trạng thái Request. | **Proposed baseline:** ít nhất 80% người tham gia usability test hoàn thành từng tác vụ mà không cần người hướng dẫn thao tác. Tối thiểu 5 người tham gia thử nghiệm; cần xác nhận số lượng với nhóm/Sponsor. | Tổ chức usability test theo từng kịch bản. Ghi nhận số người hoàn thành độc lập từng tác vụ, số người cần trợ giúp và các lỗi thao tác phát sinh. Tính tỷ lệ hoàn thành độc lập cho từng tác vụ trên tổng số người tham gia. | M01 |
| `NFR-USE-02` | Staff có thể tìm Request được giao, cập nhật Status và ghi nhận hoạt động xử lý. | **Proposed baseline:** ít nhất 80% người tham gia usability test hoàn thành các tác vụ được giao mà không cần trợ giúp. Tối thiểu 5 người tham gia thử nghiệm; cần xác nhận. | Tổ chức usability test theo từng kịch bản. Ghi nhận số người hoàn thành độc lập từng tác vụ, số người cần trợ giúp và các lỗi thao tác phát sinh. Tính tỷ lệ hoàn thành độc lập cho từng tác vụ trên tổng số người tham gia. | M02 |
| `NFR-USE-03` | Các trạng thái Request và thông tin cần người dùng hành động phải được trình bày rõ ràng. | 100% Status được sử dụng trong prototype phải có nhãn hiển thị nhất quán với danh mục trong request-status.md. Các Status yêu cầu Student bổ sung thông tin phải có hướng dẫn hành động rõ ràng. | Kiểm tra toàn bộ màn hình có hiển thị Status; đối chiếu với danh mục trạng thái và kiểm thử workflow WF-04. | M01, M02 |

## 3. Compatibility and Localization

| ID | Yêu cầu | Ngưỡng đo | Cách đo | Áp dụng cho |
| --- | --- | --- | --- | --- |
| `NFR-COMP-01` | Giao diện phải sử dụng được trên máy tính và thiết bị di động. | Các màn hình thuộc các workflow chính phải hiển thị và cho phép hoàn thành thao tác trên viewport desktop 1366 × 768 và mobile 360 × 800. Không có thành phần chức năng chính bị che khuất hoặc tràn ngang làm cản trở thao tác. Các viewport là Proposed baseline. | M01, M02, M03, M04 |
| `NFR-COMP-02` | Hệ thống phải xem xét hỗ trợ tiếng Việt và tiếng Anh theo ràng buộc kỹ thuật của đề bài. | Các màn hình chính trong phạm vi prototype phải có khả năng hiển thị nội dung tiếng Việt và tiếng Anh theo phạm vi ngôn ngữ được nhóm thống nhất. | Chuyển lần lượt hai ngôn ngữ; đối chiếu danh sách màn hình và kiểm tra nội dung không bị thiếu, cắt hoặc tràn giao diện. | M01, M02, M03, M04 |

## 4. Security and Privacy

| ID | Yêu cầu | Ngưỡng đo | Cách đo | Áp dụng cho |
| --- | --- | --- | --- | --- |
| `NFR-SEC-01` | Người dùng chỉ được truy cập chức năng phù hợp với Role đã xác thực. | 100% test case truy cập trái phép trong Role Permission Matrix phải bị từ chối. | Kiểm thử các cặp Role/chức năng; thử truy cập bằng giao diện và URL/API trực tiếp nếu prototype có API; ghi nhận kết quả từng test case. | M04; áp dụng xuyên suốt M01–M03 |
| `NFR-SEC-02` | Student chỉ được xem Request và Attachment thuộc tài khoản của mình. | 100% trường hợp Student thử truy cập Request hoặc Attachment của Student khác phải bị từ chối; không để lộ nội dung dữ liệu bị hạn chế. | Dùng tối thiểu hai tài khoản Student giả lập. Thử truy cập Request và Attachment của tài khoản khác thông qua danh sách, đường dẫn trực tiếp và API nếu prototype có API. Kiểm tra cả nội dung dữ liệu và thông tin nhạy cảm có thể bị lộ qua phản hồi lỗi. | M01, M04 |
| `NFR-SEC-03` | Staff chỉ được truy cập Request thuộc Department, phạm vi phân công hoặc quyền truy cập được cấp cho tài khoản đó. | 100% test case truy cập Request ngoài phạm vi quyền của Staff phải bị từ chối. | Dùng các tài khoản Staff giả lập thuộc phạm vi phân công khác nhau; thử xem và cập nhật Request ngoài phạm vi. | M02, M04 |
| `NFR-SEC-04` | Management chỉ được truy cập Dashboard, báo cáo và chức năng quản lý theo quyền được cấp. | 100% test case truy cập chức năng hoặc dữ liệu ngoài quyền Management được cấu hình phải bị từ chối. | Kiểm thử quyền của Management trên Dashboard, báo cáo và chức năng quản lý; đối chiếu với Role Permission Matrix. | M03, M04 |
| `NFR-SEC-05` | Các hoạt động quan trọng và thay đổi dữ liệu cần có thông tin phục vụ audit. | 100% sự kiện quan trọng được xác định trong FR-SEC-02 phải ghi nhận được actor, action, timestamp và đối tượng/thông tin thay đổi tương ứng. | Thực hiện các thao tác được liệt kê trong FR-SEC-02, bao gồm thay đổi Status, Priority, Assignment và thông tin xử lý. Đối chiếu từng thao tác với Audit Log để kiểm tra actor, action, timestamp và đối tượng/thông tin thay đổi tương ứng. | M04 |
| `NFR-SEC-06` | Thời gian lưu trữ dữ liệu và cách xử lý dữ liệu nhạy cảm phải tuân theo chính sách được Aurora University phê duyệt. | Cần xác nhận: thời hạn lưu trữ, quy tắc archive/deletion và phân loại dữ liệu nhạy cảm phải tuân theo chính sách được Aurora University phê duyệt. Sau khi chính sách được xác nhận, 100% loại dữ liệu thuộc phạm vi phải có quy tắc lưu trữ và xử lý tương ứng. | Đối chiếu cấu hình và tài liệu Data Retention/Data Handling với chính sách được Sponsor phê duyệt; kiểm tra mẫu dữ liệu theo từng loại. | M04 |
| `NFR-SEC-07` | Prototype và testing không sử dụng dữ liệu cá nhân thật của sinh viên. | 100% dữ liệu được sử dụng trong prototype và test phải là dữ liệu giả lập; không có bản ghi dữ liệu cá nhân thật trong bộ dữ liệu kiểm thử. | Kiểm tra nguồn tạo dữ liệu, bộ seed/test data và dữ liệu được nạp vào môi trường prototype. | Tất cả module |

## 5. Reliability and Data Integrity

| ID | Yêu cầu | Ngưỡng đo | Cách đo | Áp dụng cho |
| --- | --- | --- | --- | --- |
| `NFR-REL-01` | Dữ liệu Request phải được bảo toàn khi chuyển Request sang Staff hoặc Department khác. | 100% lần Transfer trong bộ test phải giữ nguyên Request ID, nội dung Request, Attachment và lịch sử xử lý trước Transfer; Assignment mới phải được ghi nhận. | Thực hiện WF-05 với nhiều trường hợp chuyển Request giữa Staff hoặc Department. So sánh Request ID, nội dung, Attachment, lịch sử xử lý và Assignment trước và sau Transfer; xác nhận Department/Staff nhận mới được ghi nhận chính xác. | M02, M04 |
| `NFR-REL-02` | Thay đổi Status, Priority, Assignment và hoạt động xử lý phải được ghi nhận nhất quán. | 100% thao tác cập nhật thành công trong test phải có bản ghi lịch sử tương ứng; không có lịch sử ghi nhận một thay đổi chưa thực sự được lưu. | Thực hiện các thao tác cập nhật; đối chiếu trạng thái/dữ liệu hiện tại với Request History và Audit Log. | M02, M04 |
| `NFR-REL-03` | Request phải tuân thủ Status Flow đã xác định trong tài liệu domain. | 100% chuyển trạng thái hợp lệ trong test được chấp nhận; 100% chuyển trạng thái không hợp lệ bị từ chối và không làm thay đổi Status hiện tại. | Kiểm thử các chuyển trạng thái theo `request-status.md`, gồm luồng bổ sung thông tin và đóng Request. | M01, M02, M04 |
| `NFR-REL-04` | Feedback phải được liên kết đúng với Request và được lưu để phục vụ báo cáo. | 100% Feedback gửi thành công trong test được liên kết với đúng Request và có thể truy xuất lại; không có Feedback gắn nhầm Request. | Gửi Feedback cho nhiều Request giả lập; đối chiếu Request ID, nội dung, Rating và dữ liệu hiển thị trong Management Reporting. | M01, M03 |

## 6. Measurement Conditions and Open Decisions

Các phép đo hiệu năng và usability phải được thực hiện trên cùng một môi trường prototype, cùng bộ dữ liệu giả lập và cùng cấu hình kiểm thử để kết quả có thể so sánh. Nhóm cần ghi lại ngày kiểm thử, phiên bản prototype, cấu hình môi trường, số lượng dữ liệu, số phiên người dùng, kết quả đo và các lỗi phát sinh.

| Nội dung cần xác nhận | Lý do | Người cần xác nhận |
| --- | --- | --- |
| Các ngưỡng Proposed baseline về thời gian phản hồi, số phiên đồng thời và quy mô dữ liệu | Đề bài không quy định các con số này; chúng đang được dùng làm ngưỡng kiểm thử prototype đề xuất. | Project Sponsor và Project Management Team |
| Số lượng người tham gia usability test | Tài liệu nguồn không quy định cỡ mẫu usability test. | Project Management Team và đại diện người dùng |
| Viewport kiểm thử desktop/mobile | Đề bài yêu cầu hỗ trợ hai loại thiết bị nhưng không chỉ định kích thước màn hình. | Project Management Team |
| Chính sách lưu trữ và xử lý dữ liệu nhạy cảm | Đề bài yêu cầu phải xem xét retention và sensitive data nhưng không nêu thời hạn hoặc chính sách cụ thể. | Aurora University / Project Sponsor |
| SLA hoặc thời gian xử lý mục tiêu dùng để xác định Request quá hạn | Module M03 nhắc đến thời gian xử lý được cấu hình nhưng nguồn chưa quy định giá trị cụ thể. | Aurora University / Project Sponsor |

## 7. Scope Limitations

- Các ngưỡng hiệu năng trong tài liệu này áp dụng cho prototype và dữ liệu mô phỏng, không phải cam kết chịu tải production.
- Kiểm thử không nhằm chứng minh khả năng vận hành đồng thời cho toàn bộ khoảng 3.000 sinh viên của Aurora University.
- Việc tích hợp thực tế với toàn bộ hệ thống hiện có của trường, triển khai production toàn trường và sử dụng dữ liệu cá nhân thật nằm ngoài phạm vi hiện tại.
- Các chính sách chưa được nguồn quy định phải được xác nhận trước khi trở thành điều kiện nghiệm thu chính thức.

## 8. Related Documents

- [Functional Requirements](./functional-requirements.md)
- [M01 – Student Portal](../03-modules/M01-student-portal/prd.md)
- [M02 – Staff Workspace](../03-modules/M02-staff-workspace/prd.md)
- [M03 – Management Dashboard](../03-modules/M03-management-dashboard/prd.md)
- [M04 – Security and Access](../03-modules/M04-security-and-access/prd.md)
- [Request Status](../02-domain/request-status.md)
- [Business Rules](../02-domain/business-rules.md)
- [Test Scenarios](../06-acceptance/test-scenarios.md)
- [Traceability Matrix](../06-acceptance/traceability-matrix.md)
