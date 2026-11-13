# Test Scenarios

## 1. Purpose

Tài liệu này mô tả các kịch bản kiểm thử dùng để xác minh từng Acceptance Criteria (AC) trong `functional-requirements.md` và các Non-Functional Requirements (NFR) trong `non-functional-requirements.md` của hệ thống UniSupport.

Các kịch bản tập trung vào phạm vi prototype, sử dụng dữ liệu giả lập và tuân theo các quy trình nghiệp vụ đã được xác định trong Workflows và tài liệu domain. Mỗi AC/NFR có ít nhất một Test Scenario tham chiếu trực tiếp để hỗ trợ kiểm thử và Traceability.

## 2. Test Conditions

- Sử dụng tài khoản và dữ liệu giả lập; không sử dụng dữ liệu cá nhân thật của sinh viên.
- Chuẩn bị tài khoản thuộc ba Role: Student, Staff và Management; tạo dữ liệu thuộc nhiều Department và phạm vi Assignment.
- Chuẩn bị Request với các Status, Priority, Request Type, Attachment và Feedback khác nhau để kiểm tra cả trường hợp thành công và thất bại.
- Các Status và chuyển trạng thái phải tuân theo `request-status.md`; không tự giả định thêm Status hoặc Status Flow.
- Các thao tác nghiệp vụ phải đối chiếu với Workflow tương ứng trong `docs/04-workflows/`.
- Mỗi kịch bản phải được thực hiện với đúng Role và phạm vi quyền của tài khoản kiểm thử.
- Đối với NFR có đo lường, ghi nhận môi trường, phiên bản prototype, cấu hình, dữ liệu và số phiên người dùng.
- Các ngưỡng ghi `Proposed baseline` chỉ là ngưỡng đề xuất cho prototype; cần xác nhận trước khi dùng làm điều kiện nghiệm thu chính thức.
- Các chính sách hoặc quy tắc được ghi `Cần xác nhận` không được xem là tiêu chí nghiệm thu đã chốt.

## 3. Functional Test Scenarios

Các kịch bản dưới đây bao phủ toàn bộ AC đang có trong `functional-requirements.md`. Mã AC được giữ nguyên theo tài liệu nguồn; riêng `FR-STA-03` không có `AC-08`, vì vậy tài liệu này không tự bổ sung mã còn thiếu.

| Mã | Kiểm AC / NFR | Tiền điều kiện | Các bước | Kết quả mong đợi | Regression |
|---|---|---|---|---|---|
| `TS-001` | `FR-STU-01/AC-01` | Student đã đăng nhập và có quyền gửi Request. | Mở Submit Request; kiểm tra các trường thông tin và danh sách Request Type. | Biểu mẫu hiển thị các trường nhập thông tin và lựa chọn Request Type. | Có |
| `TS-002` | `FR-STU-01/AC-02` | Student đã mở biểu mẫu; có ít nhất một trường bắt buộc. | Để trống một trường bắt buộc và nhấn Submit. | Hệ thống không tạo Request và thông báo trường thông tin cần bổ sung. | Có |
| `TS-003` | `FR-STU-01/AC-03` | Student đã đăng nhập. | Gửi hai Request hợp lệ; ghi nhận Request ID của từng Request. | Mỗi Request được tạo có một Request ID duy nhất. | Có |
| `TS-004` | `FR-STU-01/AC-04` | Student đã mở biểu mẫu; tài liệu đính kèm không bắt buộc. | Điền đủ thông tin hợp lệ, không đính kèm tệp và nhấn Submit. | Request được tiếp nhận thành công dù không có Attachment. | Có |
| `TS-005` | `FR-STU-01/AC-05` | Student đã mở biểu mẫu; đã xác định điều kiện tệp được cấu hình. | Chọn tệp không đáp ứng điều kiện và nhấn Submit. | Hệ thống thông báo tệp không hợp lệ và không tiếp nhận tệp đó. | Có |
| `TS-006` | `FR-STU-01/AC-06` | Student đã đăng nhập và có dữ liệu hợp lệ. | Gửi Request; kiểm tra thông báo sau khi gửi. | Student nhận thông báo xác nhận Request đã được tiếp nhận thành công. | Có |
| `TS-007` | `FR-STU-02/AC-01` | Có ít nhất hai Student giả lập; mỗi tài khoản có Request riêng. | Đăng nhập bằng một Student và mở danh sách Request. | Danh sách hiển thị các Request thuộc tài khoản Student đang đăng nhập. | Có |
| `TS-008` | `FR-STU-02/AC-02` | Student có Request ở một Status xác định. | Mở danh sách hoặc Request Detail. | Status hiện tại của từng Request được hiển thị đúng với dữ liệu hệ thống. | Có |
| `TS-009` | `FR-STU-02/AC-03` | Request đã có ít nhất một lần cập nhật. | Mở Request Detail và xem Request History. | Hệ thống hiển thị lịch sử cập nhật liên quan đến Request. | Có |
| `TS-010` | `FR-STU-02/AC-04` | Request có thể được Staff cập nhật Status. | Dùng Staff cập nhật Status; quay lại tài khoản Student và kiểm tra thông báo. | Hệ thống tạo thông báo khi Status của Request thay đổi. | Có |
| `TS-011` | `FR-STU-02/AC-05` | Request được Staff chuyển sang Awaiting Information. | Staff gửi yêu cầu bổ sung thông tin; kiểm tra tài khoản Student. | Student nhận thông báo rằng Request đang chờ bổ sung thông tin theo yêu cầu của Staff. | Có |
| `TS-012` | `FR-STU-02/AC-06` | Có hai tài khoản Student và Request thuộc tài khoản thứ hai. | Đăng nhập Student thứ nhất; thử mở Request ID của Student thứ hai. | Student thứ nhất không thể truy cập Request thuộc tài khoản khác. | Có |
| `TS-013` | `FR-STU-03/AC-01` | Request thuộc Student đang đăng nhập và có trạng thái Awaiting Information. | Mở yêu cầu bổ sung; nhập thông tin được yêu cầu và gửi. | Student có thể gửi thông tin bổ sung khi Request đang được yêu cầu bổ sung thông tin. | Có |
| `TS-014` | `FR-STU-03/AC-02` | Student đã gửi thông tin bổ sung cho một Request. | Mở lại Request và kiểm tra thông tin bổ sung đã gửi. | Thông tin bổ sung được lưu vào đúng Request đã chọn. | Có |
| `TS-015` | `FR-STU-03/AC-03` | Request đã được giải quyết theo quy trình. | Mở Request đủ điều kiện và gửi Feedback. | Student có thể gửi Feedback sau khi Request được giải quyết. | Có |
| `TS-016` | `FR-STU-03/AC-04` | Request chưa đạt điều kiện gửi Feedback theo Workflow. | Mở Request chưa đủ điều kiện và thử gửi Feedback. | Hệ thống không cho phép gửi Feedback khi Request chưa đạt điều kiện theo quy trình. | Có |
| `TS-017` | `FR-STU-03/AC-05` | Student đã gửi Feedback hợp lệ. | Mở dữ liệu Feedback hoặc Request liên quan; kiểm tra nội dung và thời điểm. | Hệ thống ghi nhận nội dung Feedback và thời điểm gửi. | Có |
| `TS-018` | `FR-STU-03/AC-06` | Có Request thuộc một Student khác. | Đăng nhập Student hiện tại và thử gửi thông tin hoặc Feedback trên Request đó. | Hệ thống từ chối thao tác trên Request không thuộc tài khoản Student đang đăng nhập. | Có |
| `TS-019` | `FR-STA-01/AC-01` | Có Request mới chưa được phân loại; Staff có quyền xử lý queue. | Đăng nhập Staff và mở danh sách Request cần phân loại. | Staff có thể xem các Request đang cần phân loại. | Có |
| `TS-020` | `FR-STA-01/AC-02` | Staff mở một Request chưa được phân loại. | Kiểm tra nội dung; chọn Request Type và Priority phù hợp; lưu. | Staff có thể xác định và lưu Request Type cùng Priority cho Request. | Có |
| `TS-021` | `FR-STA-01/AC-03` | Request đã có thông tin cần thiết để phân loại. | Chọn Department phù hợp và xác nhận phân công. | Request được phân công đến Department được chọn. | Có |
| `TS-022` | `FR-STA-01/AC-04` | Có Department và Staff phù hợp trong dữ liệu giả lập. | Chọn Staff chịu trách nhiệm và lưu Assignment. | Request ghi nhận Staff được chỉ định chịu trách nhiệm. | Có |
| `TS-023` | `FR-STA-01/AC-05` | Request chưa có đủ thông tin phân công bắt buộc. | Để trống thông tin Assignment bắt buộc và thực hiện xác nhận. | Hệ thống không xác nhận Assignment và thông báo thông tin còn thiếu. | Có |
| `TS-024` | `FR-STA-01/AC-06` | Request đã có Classification hoặc Assignment. | Thay đổi Request Type, Priority, Department hoặc Assigned Staff; xem lịch sử. | Lịch sử thay đổi Classification và Assignment được ghi nhận. | Có |
| `TS-025` | `FR-STA-02/AC-01` | Staff có Request được phân công trong phạm vi quyền. | Đăng nhập Staff và mở Request Queue. | Staff xem được danh sách Request thuộc phạm vi được phân công. | Có |
| `TS-026` | `FR-STA-02/AC-02` | Queue có Request với Status và Priority đã xác định. | Mở danh sách Request và kiểm tra các thông tin Status, Priority. | Status và Priority của từng Request được hiển thị. | Có |
| `TS-027` | `FR-STA-02/AC-03` | Queue có Request ở nhiều Status. | Chọn một Status làm điều kiện lọc. | Danh sách chỉ hiển thị các Request phù hợp với Status đã chọn. | Có |
| `TS-028` | `FR-STA-02/AC-04` | Queue có Request ở nhiều Priority. | Chọn một Priority làm điều kiện lọc. | Danh sách chỉ hiển thị các Request phù hợp với Priority đã chọn. | Có |
| `TS-029` | `FR-STA-02/AC-05` | Request có thời điểm tiếp nhận được lưu. | Mở Queue và kiểm tra thông tin thời gian chờ của Request. | Hệ thống hiển thị thời gian chờ của Request dựa trên dữ liệu thời gian đã ghi nhận. | Có |
| `TS-030` | `FR-STA-02/AC-06` | Có Request ngoài phạm vi Department/Assignment của Staff. | Đăng nhập Staff và thử tìm hoặc mở Request ngoài phạm vi. | Staff không thể xem Request ngoài phạm vi quyền truy cập. | Có |
| `TS-031` | `FR-STA-03/AC-01` | Staff được phân công một Request có lịch sử xử lý. | Mở Request Detail và kiểm tra nội dung cùng lịch sử xử lý. | Staff xem được nội dung và lịch sử xử lý của Request được phân công. | Có |
| `TS-032` | `FR-STA-03/AC-02` | Staff có Request được phân công và quyền cập nhật. | Thực hiện một chuyển Status hợp lệ theo request-status.md. | Hệ thống cho phép Staff cập nhật Status theo Status Flow. | Có |
| `TS-033` | `FR-STA-03/AC-03` | Staff đang xử lý Request. | Nhập nội dung hoạt động xử lý và lưu Activity Log. | Nội dung xử lý được ghi nhận vào Activity Log của Request. | Có |
| `TS-034` | `FR-STA-03/AC-04` | Request đang được Staff xử lý và cần Student bổ sung thông tin. | Staff nhập nội dung cần bổ sung và gửi yêu cầu cho Student. | Staff có thể gửi yêu cầu bổ sung thông tin cho Student. | Có |
| `TS-035` | `FR-STA-03/AC-05` | Request được Staff yêu cầu bổ sung thông tin. | Gửi yêu cầu bổ sung và kiểm tra Status của Request. | Request chuyển sang trạng thái chờ bổ sung thông tin phù hợp với request-status.md. | Có |
| `TS-036` | `FR-STA-03/AC-06` | Staff có Request cần chuyển sang Department khác. | Chọn Department tiếp nhận, nhập lý do Transfer nếu Workflow yêu cầu và xác nhận. | Staff có thể Transfer Request sang Department khác theo quy trình. | Có |
| `TS-037` | `FR-STA-03/AC-07` | Request có nội dung, Attachment và lịch sử trước Transfer. | Ghi nhận dữ liệu trước Transfer; thực hiện Transfer; mở Request tại nơi nhận. | Thông tin và lịch sử xử lý trước Transfer được bảo toàn. | Có |
| `TS-038` | `FR-STA-03/AC-09` | Request chưa đáp ứng điều kiện giải quyết. | Staff thử thực hiện thao tác đóng Request. | Hệ thống không cho phép đóng Request khi chưa đáp ứng điều kiện giải quyết. | Có |
| `TS-039` | `FR-STA-03/AC-10` | Staff có thể thực hiện các hoạt động xử lý trên Request. | Thực hiện cập nhật Status, ghi Activity hoặc Transfer; kiểm tra bản ghi tương ứng. | Hệ thống ghi nhận thời điểm và người thực hiện các hoạt động xử lý. | Có |
| `TS-040` | `FR-STA-03/AC-11` | Request đang ở Awaiting Information và Student có thể bổ sung. | Student gửi đầy đủ thông tin được yêu cầu; Staff mở lại Request. | Request có thể chuyển từ Awaiting Information sang In Progress sau khi nhận đủ thông tin. | Có |
| `TS-041` | `FR-MGT-01/AC-01` | Có dữ liệu Request mới trong bộ dữ liệu giả lập. | Đăng nhập Management và mở Dashboard. | Dashboard hiển thị đúng tổng số Request mới theo dữ liệu nguồn. | Có |
| `TS-042` | `FR-MGT-01/AC-02` | Có Request đang xử lý trong dữ liệu giả lập. | Mở Dashboard và đối chiếu số Request đang xử lý với dữ liệu nguồn. | Dashboard hiển thị đúng số lượng Request đang xử lý. | Có |
| `TS-043` | `FR-MGT-01/AC-03` | Có ít nhất một Request quá hạn theo thời gian mục tiêu cấu hình. | Mở khu vực theo dõi Request quá hạn. | Dashboard hiển thị danh sách Request quá hạn. | Có |
| `TS-044` | `FR-MGT-01/AC-04` | Đã cấu hình thời gian xử lý mục tiêu; có Request trước và sau ngưỡng. | Đối chiếu thời điểm tiếp nhận/tiến độ với thời gian mục tiêu; kiểm tra kết quả xác định quá hạn. | Hệ thống xác định Request quá hạn dựa trên thời gian xử lý mục tiêu được cấu hình. | Có |
| `TS-045` | `FR-MGT-01/AC-05` | Có Request được xác định là quá hạn. | Mở Dashboard và kiểm tra khu vực cảnh báo. | Hệ thống hiển thị cảnh báo đối với Request quá hạn. | Có |
| `TS-046` | `FR-MGT-01/AC-06` | Management có quyền xem chi tiết một số Request. | Mở chi tiết Request thuộc phạm vi quyền; thử mở Request ngoài phạm vi nếu có dữ liệu. | Management truy cập được thông tin chi tiết trong phạm vi được cấp quyền và không vượt quyền. | Có |
| `TS-047` | `FR-MGT-02/AC-01` | Có Request đã được ghi nhận thời điểm tiếp nhận và hoàn tất. | Mở báo cáo thời gian xử lý; đối chiếu một số bản ghi với dữ liệu nguồn. | Hệ thống cung cấp số liệu về thời gian xử lý Request dựa trên dữ liệu đã ghi nhận. | Có |
| `TS-048` | `FR-MGT-02/AC-02` | Có Request thuộc nhiều Request Type. | Mở báo cáo theo Request Type và đối chiếu số lượng từng loại. | Hệ thống cung cấp thống kê Request theo Request Type chính xác với dữ liệu nguồn. | Có |
| `TS-049` | `FR-MGT-02/AC-03` | Có Request được phân công cho nhiều Department. | Mở báo cáo workload theo Department và đối chiếu dữ liệu. | Hệ thống cung cấp thống kê khối lượng công việc theo Department. | Có |
| `TS-050` | `FR-MGT-02/AC-04` | Có Feedback giả lập đã được gửi. | Mở khu vực báo cáo Feedback. | Hệ thống hiển thị dữ liệu Feedback phục vụ đánh giá chất lượng dịch vụ. | Có |
| `TS-051` | `FR-MGT-02/AC-05` | Có bộ Request giả lập đã được ghi nhận. | Mở báo cáo và đối chiếu số liệu tổng hợp với các Request nguồn. | Dữ liệu báo cáo được tổng hợp dựa trên các Request đã được ghi nhận. | Có |
| `TS-052` | `FR-MGT-02/AC-06` | Chuẩn bị chỉ số cần dữ liệu mà bộ dữ liệu hiện tại chưa đáp ứng. | Mở hoặc yêu cầu tính chỉ số đó. | Hệ thống thông báo khi dữ liệu chưa đủ để tính toán chỉ số. | Có |
| `TS-053` | `FR-SEC-01/AC-01` | Có tài khoản Student giả lập đã xác thực. | Đăng nhập Student; mở chức năng và dữ liệu dành cho Student; thử chức năng Staff/Management. | Student chỉ truy cập được chức năng và dữ liệu dành cho Student. | Có |
| `TS-054` | `FR-SEC-01/AC-02` | Có tài khoản Staff giả lập với phạm vi quyền xác định. | Đăng nhập Staff; truy cập chức năng và Request trong phạm vi; thử ngoài phạm vi. | Staff chỉ truy cập chức năng và dữ liệu thuộc phạm vi trách nhiệm được cấp. | Có |
| `TS-055` | `FR-SEC-01/AC-03` | Có tài khoản Management giả lập với quyền được cấu hình. | Đăng nhập Management; mở chức năng quản lý được cấp và thử chức năng ngoài quyền. | Management chỉ truy cập chức năng quản lý theo quyền được cấp. | Có |
| `TS-056` | `FR-SEC-01/AC-04` | Có ít nhất một thao tác ngoài quyền của từng Role. | Đăng nhập từng Role và thử thao tác trái quyền qua giao diện; thử URL/API trực tiếp nếu prototype hỗ trợ. | Hệ thống từ chối thao tác truy cập ngoài quyền hạn của người dùng. | Có |
| `TS-057` | `FR-SEC-01/AC-05` | Management có quyền xem thông tin người dùng và Role. | Đăng nhập Management; mở danh sách/thông tin người dùng và Role. | Management xem được thông tin người dùng và Role hiện tại theo quyền được cấp. | Có |
| `TS-058` | `FR-SEC-01/AC-06` | Management có quyền cập nhật Role; có tài khoản giả lập để thử. | Chọn tài khoản; cập nhật Role theo cấu hình được phép; kiểm tra kết quả. | Management cập nhật được Role của người dùng theo quyền được cấp. | Có |
| `TS-059` | `FR-SEC-02/AC-01` | Có Request và quyền thực hiện thay đổi Status. | Thay đổi Status hợp lệ; mở Audit Log và tìm sự kiện tương ứng. | Thay đổi Status quan trọng được ghi nhận trong Audit Log. | Có |
| `TS-060` | `FR-SEC-02/AC-02` | Có Request và quyền thay đổi Priority/Assignment. | Thay đổi Priority và Assignment; kiểm tra Audit Log. | Các thay đổi Priority và Assignment được ghi nhận trong Audit Log. | Có |
| `TS-061` | `FR-SEC-02/AC-03` | Có tài khoản thực hiện thao tác và Request thử nghiệm. | Thực hiện thao tác quan trọng; kiểm tra actor, action, timestamp và thông tin đối tượng/thay đổi. | Bản ghi Audit Log có người thực hiện, thao tác, thời điểm và thông tin liên quan đến Request. | Có |
| `TS-062` | `FR-SEC-02/AC-04` | Có Audit Log và tài khoản không được cấp quyền truy cập. | Đăng nhập tài khoản không có quyền; thử mở Audit Log qua giao diện và đường dẫn trực tiếp nếu có. | Người dùng không đủ quyền không thể truy cập thông tin Audit Log. | Có |

## 4. Non-Functional Test Scenarios

Các kịch bản NFR sử dụng đúng ngưỡng và phương pháp đo đã nêu trong `non-functional-requirements.md`. Với các ngưỡng `Proposed baseline`, kết quả cần được ghi nhận để đánh giá prototype nhưng chưa được xem là cam kết production hoặc baseline nghiệm thu đã được Sponsor phê duyệt.

| Mã | Kiểm AC / NFR | Tiền điều kiện | Các bước | Kết quả mong đợi | Regression |
|---|---|---|---|---|---|
| `TS-063` | `NFR-PERF-01` | Môi trường prototype ổn định; có 1.000 Request giả lập và tối đa 10 phiên người dùng đồng thời. | Chạy lặp thao tác mở Request Form, gửi Request và xem Request Detail; đo thời gian từ lúc thao tác đến khi kết quả hiển thị hoàn chỉnh. | Ghi nhận tỷ lệ lượt thao tác hoàn tất trong không quá 3 giây; Proposed baseline là ít nhất 95%. | Có |
| `TS-064` | `NFR-PERF-02` | Có 1.000 Request giả lập, tối đa 10 phiên đồng thời và tài khoản Management. | Chạy lặp thao tác mở Dashboard và từng báo cáo; đo thời gian đến khi dữ liệu/biểu đồ hiển thị hoàn chỉnh. | Ghi nhận tỷ lệ lượt tải hoàn tất trong không quá 5 giây; Proposed baseline là ít nhất 95%. | Có |
| `TS-065` | `NFR-PERF-03` | Có bộ dữ liệu giả lập đã thống nhất, gồm nhiều Status và Request Type, có trường hợp không có dữ liệu. | Truy vấn, lọc và tổng hợp dữ liệu; đối chiếu danh sách và số liệu Dashboard/báo cáo với dữ liệu nguồn. | 100% bản ghi trong bộ dữ liệu kiểm thử được truy vấn, lọc và tổng hợp đúng; quy mô nghiệm thu chính thức vẫn cần xác nhận. | Có |
| `TS-066` | `NFR-USE-01` | Có prototype và người tham gia usability test; số lượng tối thiểu 5 người là Proposed baseline cần xác nhận. | Yêu cầu từng người tự thực hiện tác vụ gửi Request và xem Status; không hướng dẫn thao tác; ghi nhận hoàn thành và trợ giúp. | Tính tỷ lệ hoàn thành độc lập cho từng tác vụ; Proposed baseline ít nhất 80% người tham gia hoàn thành từng tác vụ. | Có |
| `TS-067` | `NFR-USE-02` | Có prototype Staff Workspace và người tham gia usability test; số lượng tối thiểu 5 người là Proposed baseline cần xác nhận. | Yêu cầu từng người tìm Request được giao, cập nhật Status và ghi nhận hoạt động xử lý; ghi nhận trợ giúp và lỗi. | Tính tỷ lệ hoàn thành độc lập; Proposed baseline ít nhất 80% người tham gia hoàn thành các tác vụ được giao. | Có |
| `TS-068` | `NFR-USE-03` | Có Request hiển thị các Status trong prototype, gồm Request cần Student bổ sung thông tin. | Kiểm tra toàn bộ màn hình có Status; đối chiếu nhãn với `request-status.md`; chạy WF-04. | 100% Status hiển thị nhất quán với danh mục; màn hình yêu cầu bổ sung thông tin có hướng dẫn hành động rõ ràng. | Có |
| `TS-069` | `NFR-COMP-01` | Có danh sách màn hình thuộc các Workflow chính. | Kiểm tra từng màn hình tại viewport desktop 1366 × 768 và mobile 360 × 800; thực hiện thao tác chính trên từng viewport. | Các màn hình hiển thị và cho phép hoàn thành thao tác; không có thành phần chức năng chính bị che hoặc tràn ngang cản trở thao tác. Kích thước là Proposed baseline. | Có |
| `TS-070` | `NFR-COMP-02` | Prototype có phạm vi màn hình chính và nội dung tiếng Việt/tiếng Anh đã thống nhất. | Chuyển lần lượt hai ngôn ngữ; kiểm tra các màn hình chính và nội dung hiển thị. | Nội dung tiếng Việt và tiếng Anh trong phạm vi đã thống nhất không bị thiếu, cắt hoặc tràn giao diện. | Có |
| `TS-071` | `NFR-SEC-01` | Có Role Permission Matrix và tài khoản đã xác thực cho từng Role. | Kiểm thử từng cặp Role/chức năng; thử truy cập qua giao diện và URL/API trực tiếp nếu prototype có API. | 100% test case truy cập trái phép trong Role Permission Matrix bị từ chối. | Có |
| `TS-072` | `NFR-SEC-02` | Có tối thiểu hai tài khoản Student giả lập; tài khoản thứ hai có Request và Attachment. | Từ tài khoản Student thứ nhất, thử truy cập Request/Attachment của tài khoản thứ hai qua danh sách, URL trực tiếp và API nếu có. | 100% lần truy cập trái phép bị từ chối; không để lộ nội dung Request, Attachment hoặc thông tin nhạy cảm trong phản hồi. | Có |
| `TS-073` | `NFR-SEC-03` | Có các tài khoản Staff giả lập với Department/phạm vi Assignment khác nhau. | Dùng từng Staff thử xem và cập nhật Request ngoài Department hoặc phạm vi được cấp. | 100% test case truy cập Request ngoài phạm vi quyền của Staff bị từ chối. | Có |
| `TS-074` | `NFR-SEC-04` | Có Role Permission Matrix và tài khoản Management với quyền được cấu hình. | Thử truy cập Dashboard, báo cáo và chức năng quản lý ngoài quyền đã cấp. | 100% test case truy cập chức năng hoặc dữ liệu ngoài quyền Management bị từ chối. | Có |
| `TS-075` | `NFR-SEC-05` | Có danh sách sự kiện quan trọng được xác định trong FR-SEC-02. | Thực hiện thay đổi Status, Priority, Assignment và hoạt động xử lý; đối chiếu từng thao tác với Audit Log. | 100% sự kiện quan trọng có actor, action, timestamp và đối tượng/thông tin thay đổi tương ứng. | Có |
| `TS-076` | `NFR-SEC-06` | Đã có chính sách Data Retention/Data Handling được Aurora University hoặc Sponsor phê duyệt. | Đối chiếu cấu hình và tài liệu lưu trữ/xử lý dữ liệu với chính sách đã phê duyệt; kiểm tra mẫu theo từng loại dữ liệu. | 100% loại dữ liệu thuộc phạm vi có quy tắc lưu trữ và xử lý tương ứng với chính sách được phê duyệt. Nếu chưa có chính sách, đánh dấu Blocked/Needs Confirmation, không tự đặt thời hạn. | Có |
| `TS-077` | `NFR-SEC-07` | Có prototype, seed data và bộ dữ liệu kiểm thử. | Kiểm tra nguồn tạo dữ liệu, seed/test data và dữ liệu đã nạp vào môi trường prototype. | 100% dữ liệu trong prototype và testing là dữ liệu giả lập; không có bản ghi dữ liệu cá nhân thật của sinh viên. | Có |
| `TS-078` | `NFR-REL-01` | Có Request chứa nội dung, Attachment và lịch sử; có Staff/Department nhận chuyển. | Ghi nhận Request ID, nội dung, Attachment, lịch sử và Assignment trước Transfer; thực hiện WF-05; so sánh sau Transfer. | 100% lần Transfer giữ nguyên Request ID, nội dung, Attachment và lịch sử trước Transfer; Assignment mới được ghi nhận. | Có |
| `TS-079` | `NFR-REL-02` | Có Request để cập nhật Status, Priority, Assignment và Activity. | Thực hiện từng thao tác cập nhật thành công; so sánh dữ liệu hiện tại với Request History và Audit Log. | 100% thao tác cập nhật thành công có bản ghi lịch sử tương ứng; không có lịch sử ghi nhận thay đổi chưa được lưu. | Có |
| `TS-080` | `NFR-REL-03` | Có `request-status.md` và Request ở các trạng thái phù hợp để thử. | Thực hiện các chuyển trạng thái hợp lệ và không hợp lệ theo Status Flow, gồm luồng Awaiting Information → In Progress và đóng Request. | 100% chuyển trạng thái hợp lệ được chấp nhận; 100% chuyển trạng thái không hợp lệ bị từ chối và Status hiện tại không thay đổi. | Có |
| `TS-081` | `NFR-REL-04` | Có nhiều Request giả lập đủ điều kiện nhận Feedback. | Gửi Feedback cho nhiều Request; đối chiếu Request ID, nội dung, Rating và dữ liệu hiển thị trong Management Reporting. | 100% Feedback gửi thành công liên kết đúng Request và truy xuất lại được; không có Feedback gắn nhầm Request. | Có |

## 5. Test Execution Record

Khi thực hiện kiểm thử, nhóm cần ghi nhận tối thiểu các thông tin sau cho từng Test Scenario:

- Test Scenario ID.
- Requirement/AC/NFR ID được kiểm thử.
- Ngày kiểm thử và người thực hiện.
- Phiên bản prototype và môi trường kiểm thử.
- Role và dữ liệu kiểm thử được sử dụng.
- Actual Result.
- Test Status: `Pass` / `Fail` / `Blocked` / `Not Run`.
- Evidence (ảnh chụp màn hình, log hoặc kết quả đo) và Bug ID nếu có.
- Với NFR đo lường: số lần chạy, số phiên đồng thời, quy mô dữ liệu, kết quả đo và cách tính tỷ lệ.

### Test Status Guidelines

| Status | Ý nghĩa |
|---|---|
| Pass | Kết quả thực tế đáp ứng Expected Result và tiêu chí đo đã được xác nhận. |
| Fail | Kết quả thực tế không đáp ứng Expected Result hoặc tiêu chí đo đã được xác nhận. |
| Blocked | Không thể thực hiện hoặc kết luận do thiếu môi trường, dữ liệu, quyền hoặc chính sách cần xác nhận. |
| Not Run | Chưa thực hiện kiểm thử. |

## 6. Coverage Notes and Open Decisions

- Các Test Scenario `TS-001` đến `TS-006` được giữ lại từ bản hiện tại; các kịch bản tiếp theo được đánh số nối tiếp.
- Bộ Functional Test Scenarios bao phủ các AC hiện có trong `functional-requirements.md`. `FR-STA-03/AC-08` không xuất hiện trong tài liệu nguồn nên không được tự tạo.
- Bộ Non-Functional Test Scenarios bao phủ 19 NFR hiện có.
- Các ngưỡng `Proposed baseline` của NFR-PERF-01, NFR-PERF-02, NFR-USE-01, NFR-USE-02 và NFR-COMP-01 cần được xác nhận trước khi dùng làm điều kiện nghiệm thu chính thức.
- NFR-SEC-06 phụ thuộc chính sách lưu trữ và xử lý dữ liệu do Aurora University/Sponsor phê duyệt. Nếu chưa có chính sách, ghi nhận `Blocked` hoặc `Needs Confirmation`, không tự đặt thời hạn lưu trữ.
- `acceptance-criteria.md` hiện có bộ AC tổng quát `AC-01` đến `AC-14`, trong khi `functional-requirements.md` có AC riêng theo từng FR. Hai hệ mã này không được coi là cùng một mã. Việc liên kết AC tổng quát với Test Scenario cần được thể hiện trong Traceability Matrix sau khi nhóm thống nhất mapping.
- Test Scenario mô tả cách kiểm tra; kết quả Pass/Fail chỉ được điền sau khi prototype thực sự được kiểm thử. Việc có Test Scenario không đồng nghĩa chức năng đã được triển khai hoặc đã Pass.

## 7. Related Documents

- [Functional Requirements](../05-requirements/functional-requirements.md)
- [Non-Functional Requirements](../05-requirements/non-functional-requirements.md)
- [Acceptance Criteria](./acceptance-criteria.md)
- [Traceability Matrix](./traceability-matrix.md)
- [Request Status](../02-domain/request-status.md)
- [Business Rules](../02-domain/business-rules.md)
- [WF-01 – Submit Request](../04-workflows/WF-01-submit-request.md)
- [WF-02 – Classify and Assign Request](../04-workflows/WF-02-classify-and-assign.md)
- [WF-03 – Process Request](../04-workflows/WF-03-process-request.md)
- [WF-04 – Request Additional Information](../04-workflows/WF-04-request-additional-information.md)
- [WF-05 – Transfer Request](../04-workflows/WF-05-transfer-request.md)
- [WF-06 – Resolve and Close Request](../04-workflows/WF-06-resolve-and-close.md)
- [WF-07 – Feedback](../04-workflows/WF-07-feedback.md)
