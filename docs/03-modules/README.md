# Modules

## 1. Overview

UniSupport được chia thành 4 modules chính. Mỗi module đảm nhiệm một nhóm chức năng nghiệp vụ riêng, giúp phân chia phạm vi phát triển và quản lý các yêu cầu của hệ thống.

## 2. Module List

| Module | Name | Main User | Documentation |
|---|---|---|---|
| M01 | Student Portal | Student | [M01](M01-student-portal/) |
| M02 | Staff Workspace | Staff | [M02](M02-staff-workspace/) |
| M03 | Management Dashboard | Management | [M03](M03-management-dashboard/) |
| M04 | Security and Access | Student, Staff, Management | [M04](M04-security-and-access/) |

## 3. Module Dependencies

- M01 cung cấp Request và Feedback cho các hoạt động quản lý.
- M02 tiếp nhận và xử lý Request từ M01.
- M03 sử dụng dữ liệu từ M01 và M02 để tạo báo cáo quản lý.
- M04 hỗ trợ kiểm soát quyền truy cập xuyên suốt hệ thống.

## 4. Documentation Structure

Mỗi module có hai tài liệu chính:

- `README.md`: Giới thiệu module, actors và dependencies.
- `prd.md`: Mô tả chi tiết Product Requirements của module.