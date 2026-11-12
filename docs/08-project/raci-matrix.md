# RACI Matrix

## 1. Purpose

RACI Matrix được sử dụng để xác định trách nhiệm của từng vai trò trong các hoạt động chính của dự án UniSupport. Tài liệu giúp nhóm hiểu rõ ai trực tiếp thực hiện công việc, ai chịu trách nhiệm cuối cùng, ai cần được tham khảo ý kiến và ai cần được thông báo.

RACI Matrix áp dụng cho 4 roles đã được xác định trong Project Proposal:

- Project Manager (PM)
- Business Analyst (BA)
- Front-end Developer (FE)
- Back-end Developer (BE)

## 2. RACI Definitions

| Symbol | Full Name | Description |
|---|---|---|
| R | Responsible | Người trực tiếp thực hiện công việc và tạo ra kết quả được yêu cầu. |
| A | Accountable | Người chịu trách nhiệm cuối cùng về kết quả và đảm bảo công việc được hoàn thành. |
| C | Consulted | Người được tham khảo ý kiến hoặc cung cấp thông tin chuyên môn trong quá trình thực hiện. |
| I | Informed | Người cần được thông báo về tiến độ, quyết định hoặc kết quả công việc. |

**General Rules:**
- Mỗi hoạt động cần có ít nhất một người Responsible (R).
- Mỗi hoạt động chỉ có một người Accountable (A) để đảm bảo trách nhiệm cuối cùng được xác định rõ ràng.
- Một người có thể đồng thời đảm nhận cả Responsible (R) và Accountable (A).
- Consulted (C) và Informed (I) được xác định tùy theo mức độ liên quan của từng vai trò.

## 3. RACI Matrix

| Activities | PM | BA | FE | BE |
|---|:---:|:---:|:---:|:---:|
| Project Initiation & Planning | A/R | C | I | I |
| Requirements Elicitation & Analysis | C | A/R | C | C |
| Scope Definition & Requirements Baseline | A | R | C | C |
| Business Workflows & Rules Definition | C | A/R | C | C |
| System Architecture, API & Database Design | I | C | C | A/R |
| UI/UX Design & Prototype | I | C | A/R | C |
| Front-end Development | I | C | A/R | C |
| Back-end Development & Infrastructure Setup | I | C | C | A/R |
| Test Planning & Acceptance Validation | C | A/R | R | R |
| System Integration & Defect Resolution | I | C | R | A/R |
| Project Monitoring, Risk & Change Management | A/R | C | I | I |
| Final Documentation, Presentation & Handover | A | R | C | R |

## 4. Role Responsibilities

### 4.1 Project Manager (PM)

Project Manager chịu trách nhiệm điều phối và quản lý tổng thể dự án. Vai trò này tập trung vào việc lập kế hoạch, theo dõi tiến độ, quản lý rủi ro, kiểm soát thay đổi và đảm bảo các hoạt động được thực hiện theo mục tiêu đã thống nhất.

### 4.2 Business Analyst (BA)

Business Analyst chịu trách nhiệm phân tích nghiệp vụ và quản lý yêu cầu. Vai trò này tập trung vào việc xác định nhu cầu người dùng, xây dựng business workflows, business rules, acceptance criteria và hỗ trợ kiểm thử để xác nhận hệ thống đáp ứng các yêu cầu đã đặt ra.

### 4.3 Front-end Developer (FE)

Front-end Developer chịu trách nhiệm phát triển giao diện và trải nghiệm người dùng. Vai trò này bao gồm UI/UX Design ở mức phù hợp với prototype, xây dựng các giao diện cho Student, Staff và Management, đảm bảo responsive UI và phối hợp kiểm thử giao diện.

### 4.4 Back-end Developer (BE)

Back-end Developer chịu trách nhiệm xây dựng logic hệ thống và xử lý dữ liệu. Vai trò này bao gồm thiết kế API, database, authentication, role-based access control, thiết lập development environment và hỗ trợ deployment.

## 5. RACI Application & Notes

- RACI Matrix xác định trách nhiệm ở cấp độ hoạt động chính của dự án, không thay thế việc phân công từng công việc cụ thể.
- Các công việc chi tiết, người được giao thực hiện và trạng thái tiến độ sẽ được theo dõi thông qua GitHub Issues.
- Các chuyên môn như DevOps, UI/UX và Testing được phân bổ cho 4 roles hiện có, không được xem là các vị trí độc lập trong cơ cấu nhóm.
- Front-end Developer và Back-end Developer phối hợp trong quá trình System Integration & Defect Resolution.
- Business Analyst chịu trách nhiệm lập kế hoạch kiểm thử và xác nhận acceptance criteria; Front-end Developer và Back-end Developer hỗ trợ thực hiện kiểm thử kỹ thuật và xử lý lỗi.

RACI Matrix có thể được điều chỉnh nếu có thay đổi được thống nhất về cơ cấu vai trò hoặc phạm vi công việc của dự án.