# WF-08 — Request Reopening (Proposed)

> **Status: Proposed — excluded from current baseline pending Sponsor/Client and team confirmation.** This workflow is a draft for documenting the newly proposed reopening function, not an approved process.

## 1. Purpose

Mô tả cách Student đề nghị xem xét lại một Request đã Closed khi không hài lòng với kết quả, và cách Staff ghi nhận quyết định.

## 2. Actors

- Primary Actor: Student
- Supporting Actor: Staff
- System

## 3. Trigger

Student không hài lòng với kết quả xử lý của Request đã Closed và gửi yêu cầu Reopening.

## 4. Preconditions

- Student đã đăng nhập.
- Request ở trạng thái `Closed` và thuộc tài khoản Student.

## 5. Proposed Main Flow

1. Student mở Request đã Closed.
2. Student chọn chức năng yêu cầu xem xét lại và nhập lý do (nếu trường lý do được xác nhận là bắt buộc).
3. Student gửi yêu cầu Reopening.
4. Hệ thống ghi nhận yêu cầu, liên kết với Request và hiển thị yêu cầu cho Staff có trách nhiệm.
5. Staff xem xét yêu cầu và ghi nhận quyết định chấp nhận hoặc từ chối.
6. Hệ thống lưu quyết định và lịch sử thao tác.
7. Nếu được chấp nhận, Request được đưa trở lại trạng thái xử lý phù hợp theo Status Flow đã được xác nhận; nếu bị từ chối, Request giữ trạng thái `Closed` và kết quả xem xét được ghi nhận.

## 6. Alternative Flow — Reopening Rejected

1. Staff từ chối yêu cầu Reopening.
2. Hệ thống ghi nhận quyết định từ chối và thông tin liên quan.
3. Request vẫn ở trạng thái `Closed`.

## 7. Error / Exception Flows

- Student cố yêu cầu Reopening cho Request không thuộc tài khoản: hệ thống từ chối thao tác.
- Request không ở trạng thái `Closed`: hệ thống không tiếp nhận yêu cầu Reopening.

## 8. Proposed Business Rules

- Student chỉ yêu cầu Reopening cho Request thuộc tài khoản của mình và đang `Closed`.
- Staff có trách nhiệm xem xét và ghi nhận quyết định.
- Quyết định được lưu để theo dõi/audit.
- Status quay lại sau khi chấp nhận Reopening cần được xác nhận; workflow này không tự quyết định tên Status hoặc quyền/định tuyến Staff.

## 9. Related Requirements

- FR-STU-03/AC-07–AC-10
- BR-06–BR-09 trong FR-STU-03
- TS-083–TS-086

**End of Proposed Workflow**
