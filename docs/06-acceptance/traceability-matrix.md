# Traceability Matrix

## 1. Purpose

Traceability Matrix được sử dụng để theo dõi mối liên hệ giữa Acceptance Criteria, Test Scenarios, Parent Tasks trong Work Breakdown Structure (WBS), Project Milestones và Quotation.

Tài liệu giúp nhóm kiểm tra:
- Mỗi Acceptance Criteria đã có Test Scenario tương ứng hay chưa.
- Các Test Scenario được thực hiện trong WBS task nào.
- Requirement thuộc Milestone nào.
- Effort hoặc chi phí liên quan được tham chiếu đến mã Quotation nào.

## 2. Traceability Matrix

### 2.1 Functional Requirements

| Acceptance Criteria | Test Scenario | Parent task (WBS) | Milestone | Quotation |
|---|---|---|---|---|
| FR-STU-01 / AC-01–AC-06 | TS-001–TS-006 | 3.3, 3.4 | MS-01 | Q-01 |
| FR-STU-02 / AC-01–AC-03, AC-06 | TS-007–TS-009, TS-012 | 3.3, 3.4 | MS-01 | Q-01 |
| FR-STU-02 / AC-04–AC-05 | TS-010–TS-011 | 4.4 | MS-02 | Q-01 |
| FR-STU-03 / AC-01–AC-02 | TS-013–TS-014 | 4.4 | MS-02 | Q-01 |
| FR-STU-03 / AC-03–AC-06 | TS-015–TS-018 | 5.2, 5.4 | MS-03 | Q-01 |
| FR-STA-01 / AC-01–AC-06 | TS-019–TS-024 | 4.1, 4.3 | MS-02 | Q-02 |
| FR-STA-02 / AC-01–AC-06 | TS-025–TS-030 | 4.1, 4.3 | MS-02 | Q-02 |
| FR-STA-03 / AC-01–AC-05 | TS-031–TS-035 | 4.2, 4.3 | MS-02 | Q-02 |
| FR-STA-03 / AC-06–AC-07 | TS-036–TS-037 | 5.1, 5.3 | MS-03 | Q-02 |
| FR-STA-03 / AC-09 | TS-038 | 5.3 | MS-03 | Q-02 |
| FR-STA-03 / WF-06 positive flow (workflow coverage, no separate detailed AC) | TS-063 | 5.3 | MS-03 | Q-02 |
| FR-STA-03 / AC-10–AC-11 | TS-039–TS-040 | 4.2, 4.3 | MS-02 | Q-02 |
| FR-MGT-01 / AC-01–AC-06 | TS-041–TS-046 | 6.1, 6.3 | MS-04 | Q-03 |
| FR-MGT-02 / AC-01–AC-06 | TS-047–TS-052 | 6.1, 6.3 | MS-04 | Q-03 |
| FR-SEC-01 / AC-01, AC-04 | TS-053, TS-056 | 3.2 | MS-01 | Q-04 |
| FR-SEC-01 / AC-02–AC-03 | TS-054–TS-055 | 6.2 | MS-04 | Q-04 |
| FR-SEC-01 / AC-05–AC-06 | TS-057–TS-058 | 3.2 | MS-01 | Q-04 |
| FR-SEC-02 / AC-01–AC-04 | TS-059–TS-062 | 6.2 | MS-04 | Q-04 |

**Notes:**

- FR-STA-03 hiện không có AC-08 trong tài liệu Functional Requirements. Vì vậy, bảng không tự tạo AC-08 hoặc Test Scenario tương ứng.
- FR-SEC-01 / AC-05 và AC-06 kiểm tra việc hệ thống xác định Role của User và áp dụng quyền truy cập tương ứng. Hai Acceptance Criteria này thuộc phạm vi Authentication & Access Control trong WBS 3.2, MS-01. Chức năng Management trực tiếp xem danh sách User và cập nhật Role (Role Administration) không thuộc phạm vi nghiệm thu chính thức của giai đoạn hiện tại.
- FR-STU-02 được chia thành hai phần vì các Acceptance Criteria về thông báo và yêu cầu bổ sung thông tin được thực hiện ở MS-02, trong khi các chức năng theo dõi Request thuộc MS-01.

### 2.2 Generic Acceptance Criteria Traceability

Bảng này liên kết 14 Acceptance Criteria tổng quát trong `acceptance-criteria.md` với Functional Requirements, Acceptance Criteria chi tiết trong `functional-requirements.md` và Test Scenarios. Mã `AC-01` đến `AC-14` ở đây là mã tổng quát; không được nhầm với mã AC riêng bên trong từng FR.

| Generic AC | Related FR | Detailed FR Acceptance Criteria | Test Scenario | Ghi chú |
|---|---|---|---|---|
| AC-01 – Student gửi yêu cầu đầy đủ | FR-STU-01 | AC-01, AC-03, AC-04, AC-06 | TS-001, TS-003–TS-004, TS-006 | Bao gồm hiển thị biểu mẫu, tạo Request, cho phép không đính kèm tệp và xác nhận tiếp nhận. |
| AC-02 – Student gửi yêu cầu thiếu thông tin | FR-STU-01 | AC-02, AC-05 | TS-002, TS-005 | Kiểm tra trường bắt buộc và tệp đính kèm không hợp lệ. |
| AC-03 – Staff nhận Request mới | FR-STA-01, FR-STA-02 | FR-STA-01/AC-01; FR-STA-02/AC-01–AC-02 | TS-019, TS-025–TS-026 | Kiểm tra Request mới có thể được tìm thấy trong danh sách/Queue phù hợp. |
| AC-04 – Staff phân công Request | FR-STA-01 | AC-03–AC-05 | TS-021–TS-023 | Bao gồm chọn Department, Assigned Staff và từ chối Assignment thiếu thông tin bắt buộc. |
| AC-05 – Staff thay đổi Request Status | FR-STA-03 | AC-02, AC-05 | TS-032, TS-035, TS-063 | TS-032 kiểm tra cập nhật Status; TS-035 kiểm tra chuyển sang trạng thái chờ bổ sung thông tin; TS-063 kiểm tra luồng Resolve rồi Close thành công theo WF-06. |
| AC-06 – Staff yêu cầu Student bổ sung thông tin | FR-STA-03, FR-STU-02 | FR-STA-03/AC-04–AC-05; FR-STU-02/AC-05 | TS-011, TS-034–TS-035 | Kiểm tra yêu cầu bổ sung, cập nhật trạng thái chờ và thông báo cho Student. |
| AC-07 – Student cung cấp thông tin bổ sung | FR-STU-03, FR-STA-03 | FR-STU-03/AC-01–AC-02; FR-STA-03/AC-11 | TS-013–TS-014, TS-040 | TS-040 kiểm tra Request có thể tiếp tục xử lý sau khi nhận đủ thông tin. |
| AC-08 – Staff chuyển giao Request | FR-STA-03 | AC-06–AC-07 | TS-036–TS-037 | Kiểm tra Transfer và bảo toàn thông tin/lịch sử. |
| AC-09 – Staff hoàn tất và đóng Request | FR-STA-03 | AC-09 | TS-063 | TS-063 kiểm tra luồng thành công theo WF-06: In Progress → Resolved → Closed, bao gồm lưu Resolution, Closed Date và Request History. TS-038 là Negative Test bổ trợ, kiểm tra hệ thống chặn đóng Request khi chưa đủ điều kiện. |
| AC-10 – Student kiểm tra Request | FR-STU-02 | AC-01–AC-03 | TS-007–TS-009 | Kiểm tra danh sách Request, Status hiện tại và Request History. |
| AC-11 – Management mở Management Dashboard | FR-MGT-01 | AC-01–AC-06 | TS-041–TS-046 | Kiểm tra các số liệu tổng quan và thông tin Request trên Dashboard. |
| AC-12 – User không được cấp quyền cố gắng truy cập chức năng hoặc dữ liệu | FR-SEC-01, FR-SEC-02 | FR-SEC-01/AC-01–AC-04; FR-SEC-02/AC-01–AC-04 | TS-053–TS-056, TS-059–TS-062 | Mapping bao phủ xác thực, Role/permission và bảo vệ dữ liệu/truy cập. |
| AC-13 – User thực hiện hành động cần được ghi nhận | FR-STA-03, FR-SEC-02 | FR-STA-03/AC-03, AC-10; FR-SEC-02/AC-01–AC-04 | TS-033, TS-039, TS-060–TS-062, TS-076 | TS-076 là NFR test về Audit Log; các TS khác kiểm tra Activity/Request History và ghi nhận thao tác. |
| AC-14 – Student gửi Feedback sau khi Request được xử lý | FR-STU-03, FR-MGT-02 | FR-STU-03/AC-03–AC-06; FR-MGT-02/AC-01–AC-06 | TS-015–TS-018, TS-047–TS-052, TS-082 | TS-015/017 kiểm tra gửi và lưu Feedback; TS-016/018 kiểm tra điều kiện/quyền; TS-047–052 kiểm tra báo cáo; TS-082 kiểm tra liên kết Feedback với Request. |

**Mapping notes:**

- Đây là mapping ở cấp tổng quát, được xây dựng từ cột `Related Requirements`, nội dung Scenario/Expected Result của Generic AC và Test Scenarios hiện có. Các Test Scenario có thể hỗ trợ nhiều Generic AC.
- Với AC-05, TS-063 bổ sung kiểm tra luồng cập nhật Status thành công `In Progress → Resolved → Closed` theo WF-06. Với AC-09, TS-063 là Test Scenario trực tiếp cho luồng đóng thành công; TS-038 là Negative Test bổ trợ để xác minh hệ thống chặn đóng Request khi chưa đủ điều kiện.
- Với AC-14, điều kiện gửi Feedback phải tuân theo WF-07: Request ở trạng thái `Closed`. TS-016 kiểm tra trường hợp Request chưa Closed và không được xem là bằng chứng cho luồng gửi Feedback thành công.
- Mapping này không thay thế các liên kết chi tiết theo FR trong mục 2.1.

### 2.3 Non-Functional Requirements

| Requirement | Test Scenario | Parent task (WBS) | Milestone | Quotation |
|---|---|---|---|---|
| NFR-PERF-01 | TS-064 | 3.3, 3.4, 3.5, 3.6, 4.5, 4.6 | MS-01, MS-02 | Q-01, Q-06 |
| NFR-PERF-02 | TS-065 | 6.1, 6.3, 6.5, 6.6 | MS-04 | Q-03, Q-06 |
| NFR-PERF-03 | TS-066 | 3.5, 3.6, 4.5, 4.6, 5.5, 5.6, 6.5, 6.6 | MS-01–MS-04 | Q-06 |
| NFR-USE-01 | TS-067 | 3.4, 3.5, 3.6 | MS-01 | Q-01, Q-06 |
| NFR-USE-02 | TS-068 | 4.3, 4.5, 4.6 | MS-02 | Q-02, Q-06 |
| NFR-USE-03 | TS-069 | 3.4, 4.4, 3.5, 4.5, 4.6 | MS-01, MS-02 | Q-01, Q-06 |
| NFR-COMP-01 | TS-070 | 6.4, 6.5, 6.6 | MS-04 | Q-06 |
| NFR-COMP-02 | TS-071 | 6.4, 6.5, 6.6 | MS-04 | Q-06 |
| NFR-SEC-01 | TS-072 | 3.2, 6.2, 6.5, 6.6 | MS-01, MS-04 | Q-04, Q-06 |
| NFR-SEC-02 | TS-073 | 3.2, 6.2, 3.5, 6.5, 6.6 | MS-01, MS-04 | Q-04, Q-06 |
| NFR-SEC-03 | TS-074 | 4.1, 4.3, 4.5, 4.6, 6.2 | MS-02, MS-04 | Q-02, Q-04, Q-06 |
| NFR-SEC-04 | TS-075 | 6.1, 6.2, 6.3, 6.5, 6.6 | MS-04 | Q-03, Q-04, Q-06 |
| NFR-SEC-05 | TS-076 | 4.2, 6.2, 4.5, 4.6, 6.5, 6.6 | MS-02, MS-04 | Q-02, Q-04, Q-06 |
| NFR-SEC-06 | TS-077 | TBD | TBD | TBD |
| NFR-SEC-07 | TS-078 | 3.1, 3.5, 3.6 và các giai đoạn testing | MS-01–MS-04 | Q-04, Q-06 |
| NFR-REL-01 | TS-079 | 5.1, 5.3, 5.5, 5.6 | MS-03 | Q-02, Q-06 |
| NFR-REL-02 | TS-080 | 4.2, 4.3, 5.1, 6.2, 4.5, 5.5, 6.5, 6.6 | MS-02–MS-04 | Q-02, Q-04, Q-06 |
| NFR-REL-03 | TS-081 | 4.2, 4.3, 5.1, 5.3, 4.5, 5.5, 6.5, 6.6 | MS-02–MS-04 | Q-02, Q-06 |
| NFR-REL-04 | TS-082 | 5.2, 5.4, 5.5, 5.6, 6.1 | MS-03, MS-04 (reporting regression) | Q-01, Q-03, Q-06 |

**Notes:**

- NFR-PERF-03 và một số NFR khác được kiểm thử xuyên suốt nhiều Milestones thông qua regression testing.
- NFR-SEC-06 liên quan đến Data Retention/Data Handling Policy. Nội dung này cần Sponsor xác nhận trước khi xác định WBS task, Milestone và Quotation.
- Các Test Scenario của NFR được đánh số từ TS-064 đến TS-082 theo tài liệu `test-scenarios.md`.

## 3. Milestone Reference

| Milestone | Description | Related requirements |
|---|---|---|
| MS-01 | Student submits and tracks Request | FR-STU-01, FR-STU-02, FR-SEC-01 và một số NFR liên quan |
| MS-02 | Staff intake, classification, assignment and processing | FR-STA-01, FR-STA-02, FR-STA-03, FR-STU-02, FR-STU-03 và một số NFR liên quan |
| MS-03 | Transfer, resolve, close and feedback | FR-STA-03, FR-STU-03 và một số NFR liên quan |
| MS-04 | Management Dashboard, whole-system permissions and handover | FR-MGT-01, FR-MGT-02, FR-SEC-01, FR-SEC-02 và một số NFR liên quan |

## 4. Traceability Rules

1. Mỗi Functional Requirement hoặc Non-Functional Requirement cần có ít nhất một Test Scenario tương ứng nếu đã đủ thông tin để kiểm thử.
2. Test Scenario phải tham chiếu đúng Requirement ID và Acceptance Criteria ID trong tài liệu nguồn.
3. Parent task được tham chiếu bằng WBS ID trong Master Plan. Khi GitHub Parent Issue được tạo và xác nhận, nhóm có thể bổ sung GitHub Issue ID vào bảng.
4. Milestone phải phản ánh kế hoạch thực hiện trong Master Plan, không tự gán Milestone cho các yêu cầu chưa được chốt.
5. Quotation ID phải được đối chiếu với `quotation.xlsx` trước khi xem là thông tin chính thức.
6. Khi Requirement, Acceptance Criteria, Test Scenario hoặc WBS thay đổi, nhóm cần cập nhật Traceability Matrix để bảo đảm các tài liệu thống nhất.

## 5. Items Requiring Confirmation

**Lưu ý về Quotation:** Các mã Q-xx trong bảng hiện được giữ theo mapping tham chiếu đang có trong WBS/Master Plan. Chúng chưa được xác nhận là mã báo giá chính thức cho đến khi đối chiếu được với dữ liệu hoàn chỉnh trong `quotation.xlsx`. Không sử dụng các mã này như đơn giá hoặc cam kết chi phí đã được phê duyệt.

| Item | Current status | Required action |
|---|---|---|
| NFR-SEC-06 | Chưa xác định WBS và Milestone | Xác nhận Data Retention/Data Handling Policy với Sponsor |
| Quotation Q-01–Q-08 | Chưa đối chiếu được với báo giá gốc | Kiểm tra và đồng bộ với `quotation.xlsx` |
| GitHub Parent Issue IDs | Chưa được cung cấp trong Master Plan | Bổ sung ID sau khi các Parent Issues được tạo |
| Generic AC-01–AC-14 | Đã có mapping tại mục 2.2 | Rà soát lại khi Generic AC, FR hoặc Test Scenarios thay đổi |

## 6. References

- `docs/05-requirements/functional-requirements.md`
- `docs/05-requirements/non-functional-requirements.md`
- `docs/06-acceptance/acceptance-criteria.md`
- `docs/06-acceptance/test-scenarios.md`
- `docs/08-project/master-plan.xlsx`
- `docs/08-project/quotation.xlsx`
- `docs/08-project/wbs.md`
