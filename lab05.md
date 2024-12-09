# Payroll System Class Design

## 1. User Class
- **Mục đích**: Quản lý thông tin đăng nhập người dùng (nhân viên, quản trị viên).
- **Thuộc tính**:
  - `username`: Tên đăng nhập.
  - `password`: Mật khẩu.

 
  - `role`: Vai trò của người dùng (nhân viên, quản trị viên).
- **Phương thức**:

 
  - `login()`: Xác thực đăng nhập.

- **Sơ đồ**:

  https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbkZa9eSMeHLt9EOd4ncAbGpQMWeAjG2cJc9UQcMYa4bnHbvgM31Gk0YihpYr9G18loSv1LAIZavATdvcbeMYauvGEb4lEuQhaSKlDIW7O10000__y30000
## 2. Employee Class
- **Mục đích**: Quản lý thông tin nhân viên.
- **Thuộc tính**:
  - `employeeId`: Mã số nhân viên.
  - `name`: Tên nhân viên.
  - `address`: Địa chỉ.
  - `baseSalary`: Lương cơ bản.

 
  - `allowance`: Phụ cấp.
- **Phương thức**:
  - `updateInformation()`: Cập nhật thông tin nhân viên.

-**Sơ đồ**:
https://www.planttext.com/api/plantuml/png/LCwn3S9038NX_gPm2GKBN9K2YjIPm8aDYkIpe_CTA8gOZ8AHM044297o__IAzxZT6o-OIqq2XpI9pSnX47J_9Im1O0VypPOYT2MFUdgpOk8L855czvNrwDoXO9uZxAtsmf-fY5rG1_vJW3eH5cxrQ3bX6KqtsmXd6obSGyDAhwlX2G00__y30000
## 3. TimeSheet Class
- **Mục đích**: Quản lý thời gian làm việc của nhân viên.
- **Thuộc tính**:
  - `employeeId`: Mã số nhân viên.
  - `date`: Ngày làm việc.

 
  - `hoursWorked`: Số giờ làm việc.
  - `projectCode`: Mã dự án.
- **Phương thức**:

 
  - `submitTime()`: Ghi lại thời gian làm việc.
- **Sơ đồ**:
  https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbkZa98PcvgS4PgQWbNSavYSJ62hr3DfQ2Wgv2QMv2JNvcQwfbYfH1SKfIPbmuMJaaiIRLIS06IO6v6VcbHSNX-KNOgK9bBVcbI3aIye2W_ApMvn3a_9HL9ku92SMbIRcO9o2uDJIk5ilpC5AvQBeVKl1IWaxW00000__y30000
## 4. Payroll Class
- **Mục đích**: Tính toán lương của nhân viên.
- **Thuộc tính**:
  - `employeeId`: Mã số nhân viên.
  - `salary`: Lương trước khi khấu trừ.
  - `deductions`: Các khoản khấu trừ.

 
  - `netPay`: Lương thực nhận.
- **Phương thức**:

 
  - `calculateSalary()`: Tính toán lương dựa trên bảng chấm công và thông tin nhân viên.
  - `calculateDeductions()`: Tính toán các khoản khấu trừ (thuế, bảo hiểm).

-**Sơ đồ**:

https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbkZa90OcLHVauELt9EOd4nZATGpQMWeAkGcbkGar-PckgPOgKGN5AKcPSE5YvEp4aighHISCalJSf91GkbfAQK9fTavkSLemZdfPO0JKGIKb18Jin9Bir9B4aD1fkYeObTrWLk89AAMYw7rBmKeAkv00000F__0m00
## 5. BankPayment Class
- **Mục đích**: Xử lý thanh toán lương qua ngân hàng.
- **Thuộc tính**:

 
  - `employeeId`: Mã số nhân viên.

 
  - `amount`: Số tiền thanh toán.

 
  - `transactionStatus`: Trạng thái giao dịch.
- **Phương thức**:

 
  - `processPayment()`: Thực hiện giao dịch thanh toán qua ngân hàng.
  - `sendToBank()`: Gửi yêu cầu tới ngân hàng và nhận phản hồi.
 
  - **Sơ đồ**:
  https://www.planttext.com/api/plantuml/png/JCun3i8m30NGFQVm20CNo5GX5ZQaSW7JM2WYiQlOGQegJiR0aRW29KAew_lo_tu_NvqQ5givmHxvTi8f4viR4ggk1MO7i0FAOvA9w1Wyz5OYNnjZbihcuI3ragYH5MJ5mQ9mRsXLLmS0Ov61L7_bcws7kyJG8YKEP_bE__dXkWMN7zq7003__mC0

## 6. Payslip Class
- **Mục đích**: Tạo và in phiếu lương cho nhân viên.
- **Thuộc tính**:
  - `employeeId`: Mã số nhân viên.

 
  - `payslipContent`: Nội dung phiếu lương.
- **Phương thức**:
  - `generatePayslip()`: Tạo nội dung phiếu lương dựa trên dữ liệu tính lương.
  - `printPayslip()`: In phiếu lương hoặc xuất ra file.
 
-**Sơ đồ**:

https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbkZa90OcLnJcO1Lt9EOd4nZATGpQMWeAkGcbkGar-PckgPOgKGN5AKcPSE5Yw0A7BEpoj9pIj1ab9GI4_DIorAB4c5cgEXQQLGbf-P0fOh0AegGPUevN98pKi1EeIB2m000F__0m00

## 7. Report Class
- **Mục đích**: Tạo báo cáo về lương, bảng chấm công.
- **Phương thức**:
  - `generateSalaryReport()`: Tạo báo cáo lương.
  - `generateTimeSheetReport()`: Tạo báo cáo bảng chấm công.
 
-**Sơ đồ**:

https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbkZa9GQa5-KGbNSavYSJ6Ker3DfG04wQbvgKM99Qd1YJc9HPKGAGrDAuMo_CmK50KXcRcfmHcfgILeQcgv75BpKe2MS040003__mC0

## Mối quan hệ giữa các lớp:
- **User** và **Employee**: `Employee` kế thừa từ `User`.
- **TimeSheet** cung cấp dữ liệu cho **Payroll** để tính lương.
- **Payroll** cung cấp dữ liệu cho **Payslip** để tạo phiếu lương.
- **BankPayment** xử lý giao dịch thanh toán dựa trên dữ liệu từ **Payroll**.
- **Report** cung cấp báo cáo chi tiết dựa trên dữ liệu từ **Payroll** và **TimeSheet**.

- **Sơ đồ các lớp**:

https://www.planttext.com/api/plantuml/png/X5IxRXGn5Etz5LVR094sWdP44IL1Q0kaY0sYlZk-p9XuREC7qGfIKz10JKL9nGTCaOByo7m1lu3diRFZxB9fvd5zvfnpZw_dRtrxuZnQ7oh9s2Eu-zRKNrK9gYZlVY7aVtxc89lwXs6vHEVWZICBdnZ0749yL5XH1ajlXIgweecWQsrvKhHQJb40KXT2FNwImQcEIwZO3HluNrH6wZNHe473wo8bt955pYqvbzHMw6Y94kqwWtCTLf9wg9Jw6bLEaof0C1mzBTGxRIlqGdVkFch1jzOkHKNBaiWVzjRoHEfuxLvB7Qnxg-qLySI6iVezvVvCypGQ5rQLyAtMheCBNCSevM5zjzio9nxojYcNb1Nvo9Z4aAFCWupU--1Q2_jMpqV22MAqUOhgAX9Nf1w82YiTb4yyUOlAOSUzzEY3IyA9eULncmVoCQ0kDrByKhVIUtDpKfZ3PamFEjFAKsjg8bkG8XlR7dWINHDH_lx2gFoQZBPz2bkQFjj-AU7Q0CP9kuUvQK_egwR-Bk13G0LbKt-1GZJrx-IaTcVq-UVvV7kQCbYeagpmZesrsRCP74NGxEdnyT5iCjwnzsu87TlMHd2yRyOmWvU3OSSsjIbkEWSPNFHxzn_iPekcd4Du3qWF6U-5JtlQ_O2Tn9bf_tl_0000__y30000
