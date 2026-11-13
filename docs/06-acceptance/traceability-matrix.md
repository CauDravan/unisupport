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
| FR-STA-03 / AC-06–AC-07, AC-09 | TS-036–TS-038 | 5.1, 5.3 | MS-03 | Q-02 |
| FR-STA-03 / AC-10–AC-11 | TS-039–TS-040 | 4.2, 4.3 | MS-02 | Q-02 |
| FR-MGT-01 / AC-01–AC-06 | TS-041–TS-046 | 6.1, 6.3 | MS-04 | Q-03 |
| FR-MGT-02 / AC-01–AC-06 | TS-047–TS-052 | 6.1, 6.3 | MS-04 | Q-03 |
| FR-SEC-01 / AC-01, AC-04 | TS-053, TS-056 | 3.2 | MS-01 | Q-04 |
| FR-SEC-01 / AC-02–AC-03 | TS-054–TS-055 | 6.2 | MS-04 | Q-04 |
| FR-SEC-01 / AC-05–AC-06 | TS-057–TS-058 | TBD | TBD | TBD |
| FR-SEC-02 / AC-01–AC-04 | TS-059–TS-062 | 6.2 | MS-04 | Q-04 |

**Notes:**

- FR-STA-03 hiện không có AC-08 trong tài liệu Functional Requirements. Vì vậy, bảng không tự tạo AC-08 hoặc Test Scenario tương ứng.
- FR-SEC-01 / AC-05 và AC-06 liên quan đến việc Management quản lý Roles. Master Plan hiện ghi nhận nội dung này là chưa nằm trong kế hoạch đã chốt và cần xác nhận. Do đó, Parent task, Milestone và Quotation được để là `TBD`.
- FR-STU-02 được chia thành hai phần vì các Acceptance Criteria về thông báo và yêu cầu bổ sung thông tin được thực hiện ở MS-02, trong khi các chức năng theo dõi Request thuộc MS-01.

### 2.2 Non-Functional Requirements

| Requirement | Test Scenario | Parent task (WBS) | Milestone | Quotation |
|---|---|---|---|---|
| NFR-PERF-01 | TS-063 | 3.3, 3.4, 3.5, 3.6, 4.5, 4.6 | MS-01, MS-02 | Q-01, Q-06 |
| NFR-PERF-02 | TS-064 | 6.1, 6.3, 6.5, 6.6 | MS-04 | Q-03, Q-06 |
| NFR-PERF-03 | TS-065 | 3.5, 3.6, 4.5, 4.6, 5.5, 5.6, 6.5, 6.6 | MS-01–MS-04 | Q-06 |
| NFR-USE-01 | TS-066 | 3.4, 3.5, 3.6 | MS-01 | Q-01, Q-06 |
| NFR-USE-02 | TS-067 | 4.3, 4.5, 4.6 | MS-02 | Q-02, Q-06 |
| NFR-USE-03 | TS-068 | 3.4, 4.4, 3.5, 4.5, 4.6 | MS-01, MS-02 | Q-01, Q-06 |
| NFR-COMP-01 | TS-069 | 6.4, 6.5, 6.6 | MS-04 | Q-06 |
| NFR-COMP-02 | TS-070 | 6.4, 6.5, 6.6 | MS-04 | Q-06 |
| NFR-SEC-01 | TS-071 | 3.2, 6.2, 6.5, 6.6 | MS-01, MS-04 | Q-04, Q-06 |
| NFR-SEC-02 | TS-072 | 3.2, 6.2, 3.5, 6.5, 6.6 | MS-01, MS-04 | Q-04, Q-06 |
| NFR-SEC-03 | TS-073 | 4.1, 4.3, 4.5, 4.6, 6.2 | MS-02, MS-04 | Q-02, Q-04, Q-06 |
| NFR-SEC-04 | TS-074 | 6.1, 6.2, 6.3, 6.5, 6.6 | MS-04 | Q-03, Q-04, Q-06 |
| NFR-SEC-05 | TS-075 | 4.2, 6.2, 4.5, 4.6, 6.5, 6.6 | MS-02, MS-04 | Q-02, Q-04, Q-06 |
| NFR-SEC-06 | TS-076 | TBD | TBD | TBD |
| NFR-SEC-07 | TS-077 | 3.1, 3.5, 3.6 và các giai đoạn testing | MS-01–MS-04 | Q-04, Q-06 |
| NFR-REL-01 | TS-078 | 5.1, 5.3, 5.5, 5.6 | MS-03 | Q-02, Q-06 |
| NFR-REL-02 | TS-079 | 4.2, 4.3, 5.1, 6.2, 4.5, 5.5, 6.5, 6.6 | MS-02–MS-04 | Q-02, Q-04, Q-06 |
| NFR-REL-03 | TS-080 | 4.2, 4.3, 5.1, 5.3, 4.5, 5.5, 6.5, 6.6 | MS-02–MS-04 | Q-02, Q-06 |
| NFR-REL-04 | TS-081 | 5.2, 5.4, 5.5, 5.6, 6.1 | MS-03, MS-04 (reporting regression) | Q-01, Q-03, Q-06 |

**Notes:**

- NFR-PERF-03 và một số NFR khác được kiểm thử xuyên suốt nhiều Milestones thông qua regression testing.
- NFR-SEC-06 liên quan đến Data Retention/Data Handling Policy. Nội dung này cần Sponsor xác nhận trước khi xác định WBS task, Milestone và Quotation.
- Các Test Scenario của NFR được đánh số từ TS-063 đến TS-081 theo tài liệu `test-scenarios.md`.

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

| Item | Current status | Required action |
|---|---|---|
| FR-SEC-01 / AC-05–AC-06 | Chưa được xác nhận trong Master Plan | Nhóm và Sponsor xác nhận có đưa chức năng Management quản lý Roles vào scope hay không |
| NFR-SEC-06 | Chưa xác định WBS và Milestone | Xác nhận Data Retention/Data Handling Policy với Sponsor |
| Quotation Q-01–Q-08 | Chưa đối chiếu được với báo giá gốc | Kiểm tra và đồng bộ với `quotation.xlsx` |
| GitHub Parent Issue IDs | Chưa được cung cấp trong Master Plan | Bổ sung ID sau khi các Parent Issues được tạo |
| Generic AC-01–AC-14 | Là bộ Acceptance Criteria tổng quát trong `acceptance-criteria.md` | Nhóm cần xác định cách liên kết với AC riêng của từng FR nếu muốn đưa bộ AC này vào Traceability Matrix |

## 6. References

- `docs/05-requirements/functional-requirements.md`
- `docs/05-requirements/non-functional-requirements.md`
- `docs/06-acceptance/acceptance-criteria.md`
- `docs/06-acceptance/test-scenarios.md`
- `docs/08-project/master-plan.xlsx`
- `docs/08-project/quotation.xlsx`
- `docs/08-project/wbs.md`
