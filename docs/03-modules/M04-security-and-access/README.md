# M04 – Security and Access

## 1. Purpose

Security and Access là module chịu trách nhiệm quản lý việc xác thực và phân quyền truy cập trong hệ thống UniSupport. Module bảo vệ dữ liệu Student, kiểm soát quyền sử dụng chức năng theo Role và ghi nhận các hoạt động quan trọng để phục vụ kiểm tra.

## 2. Actors

- **Student:** Truy cập các chức năng dành cho Student.
- **Staff:** Truy cập Request thuộc phạm vi được phân quyền.
- **Management:** Truy cập chức năng quản lý và báo cáo theo quyền được cấp.

## 3. Main Capabilities

- User Authentication.
- Role-Based Access Control.
- Access Permission Management.
- Audit Log Management.
- Data Access Protection.

## 4. Dependencies

- **M01 – Student Portal:** Bảo vệ quyền truy cập và dữ liệu Student.
- **M02 – Staff Workspace:** Kiểm soát quyền truy cập Request của Staff.
- **M03 – Management Dashboard:** Kiểm soát quyền truy cập chức năng và dữ liệu Management.

## 5. Related Documentation

- [PRD](prd.md)