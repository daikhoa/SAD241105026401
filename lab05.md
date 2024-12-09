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

## 7. Report Class
- **Mục đích**: Tạo báo cáo về lương, bảng chấm công.
- **Phương thức**:
  - `generateSalaryReport()`: Tạo báo cáo lương.
  - `generateTimeSheetReport()`: Tạo báo cáo bảng chấm công.

## Mối quan hệ giữa các lớp:
- **User** và **Employee**: `Employee` kế thừa từ `User`.
- **TimeSheet** cung cấp dữ liệu cho **Payroll** để tính lương.
- **Payroll** cung cấp dữ liệu cho **Payslip** để tạo phiếu lương.
- **BankPayment** xử lý giao dịch thanh toán dựa trên dữ liệu từ **Payroll**.
- **Report** cung cấp báo cáo chi tiết dựa trên dữ liệu từ **Payroll** và **TimeSheet**.
