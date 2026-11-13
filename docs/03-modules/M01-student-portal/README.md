# M01 – Student Portal

## 1. Purpose

Student Portal là module dành cho Student để gửi yêu cầu hỗ trợ, theo dõi trạng thái xử lý, cung cấp thông tin bổ sung và gửi Feedback về kết quả giải quyết yêu cầu.

## 2. Actors

- **Primary Actor:** Student.
- **Supporting Actor:** Staff (tiếp nhận và xử lý Request).

## 3. Main Capabilities

- Student Request Submission.
- Request Tracking.
- Additional Information Submission.
- Feedback Submission.

## 4. Dependencies

- **M02 – Staff Workspace:** Tiếp nhận và xử lý các Request do Student gửi.
- **M04 – Security and Access:** Kiểm soát quyền truy cập và bảo vệ dữ liệu Student.

## 5. Related Documentation

- [PRD](prd.md)