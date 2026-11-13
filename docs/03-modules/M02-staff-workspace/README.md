# M02 – Staff Workspace

## 1. Purpose

Staff Workspace là module dành cho Staff để tiếp nhận, phân loại, phân công và xử lý các Request thuộc phạm vi Department được giao. Module hỗ trợ Staff cập nhật tiến độ, yêu cầu Student bổ sung thông tin, chuyển Request và ghi nhận kết quả xử lý.

## 2. Actors

- **Primary Actor:** Staff.
- **Supporting Actor:** Student (cung cấp thông tin bổ sung khi được yêu cầu).

## 3. Main Capabilities

- View Request Queue.
- Classify and Assign Request.
- Process Request.
- Request Additional Information.
- Transfer Request.
- Resolve and Close Request.

## 4. Dependencies

- **M01 – Student Portal:** Nhận Request và thông tin bổ sung từ Student.
- **M04 – Security and Access:** Kiểm soát quyền truy cập của Staff đối với Request và dữ liệu liên quan.

## 5. Related Documentation

- [PRD](prd.md)