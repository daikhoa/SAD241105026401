# Phân Tích Kiến Trúc và Ca Sử Dụng Hệ Thống "Payroll System"
## **1. Phân tích kiến trúc**
## Đề xuất kiến trúc:
### Kiến trúc hệ thống được thiết kế theo mô hình Layered Architecture với các thành phần chính:
#### Presentation Layer (Giao diện):
- #### Cung cấp giao diện người dùng trên nền Windows Desktop.
- #### Bao gồm các chức năng nhập dữ liệu (timecard, purchase order), báo cáo và thay đổi tùy chọn.
### Application Layer (Xử lý nghiệp vụ):
- #### Quản lý luồng xử lý nghiệp vụ như tính toán lương, xác minh dữ liệu, và thực hiện thanh toán.
- #### Thực hiện giao tiếp với các hệ thống bên dưới.
### Data Access Layer (Truy cập dữ liệu):
- #### Giao tiếp với cơ sở dữ liệu Payroll và Project Management Database (DB2).
- #### Đảm bảo truy xuất dữ liệu chính xác và hiệu quả.
### Database Layer (Cơ sở dữ liệu):
- #### Lưu trữ thông tin nhân viên, timecard, đơn hàng và lịch sử thanh toán.
### Biểu đồ Sequence
![PlanText](https://www.planttext.com/api/plantuml/png/X9913e8m44NtFKN3dWkuC2JgJWs9Nc0e4qHR86qnQGWdS-6Hl88bqAe4OPRzR_xC_FJrU4PAWzIruAG2TeCCQH23aINd9wCqYe0sXDhowZaNo42cz025VH1OQCTqnJWeHHtKC_AZjtz0ItYbPrhoEtSdAbuQnDcv7hB2WbyiooioFMldc6R1QmiQ4b18zs1GJlZqYNfiubXhEGuj3DS-dqbnP3lD32Uiw1rudeB6pGLaXiTQ92Y93-nxsD1FncjtZ6iW4HPfzstU0000__y30000)
## **2. Cơ chế phân tích**
### Các cơ chế cần giải quyết:
### Tính lương tự động:
- #### Xử lý các quy tắc tính toán cho từng loại nhân viên (giờ công, lương cố định, hoa hồng).
### Quản lý thời gian làm việc:
- #### Ghi nhận và xử lý timecard theo ngày và dự án.
### Quản lý hoa hồng bán hàng:
- #### Ghi nhận đơn hàng và tính toán hoa hồng dựa trên tỷ lệ.
### Xác thực và bảo mật:
- #### Đảm bảo chỉ nhân viên mới có thể truy cập dữ liệu cá nhân.
### Tích hợp với DB2:
- #### Truy cập thông tin dự án và số tài khoản từ cơ sở dữ liệu cũ mà không làm thay đổi nó

## 3. Phân tích ca sử dụng: Payment
### Các lớp phân tích:
- #### PaymentProcessor: Thực hiện logic tính lương và tạo bản ghi thanh toán.
- #### Employee: Đại diện thông tin nhân viên, bao gồm loại nhân viên, giờ công, hoặc thông tin đơn hàng.
- #### PaymentMethod: Xử lý phương thức thanh toán (chuyển khoản, gửi bưu điện, nhận trực tiếp).
- #### PayrollDatabase: Quản lý thông tin nhân viên và lịch sử thanh toán.
### Biểu đồ Sequence
![PlanText](https://www.planttext.com/api/plantuml/png/R991QiCm44NtEeN8obda0gM44DobmIGdcCgJH21fZ3Gk-6nTz4YzGaUMdTgqscd-c_yrWxu_lqw98VBWdGB357KBOoJdhcDYzAeNpHhRGs2z4ybZu3QImPGexZGatRP_eDnV0yCx99oO-hnbtdplQCGYokNVc0RvGLt9Q9JQl4iVZXAiNtGSmYnK7J1U8DnnhqGIe3uBS4TUqbArLr8xBBtE9dvTnADoHBs-oGOGp4ClTQNb53yfIPS1PmOdMPAxpinS9fxsFOmrCbYNLXvjavMom7dEwXSiBi8yJGo5cuqUs59OsKoZ9VZ0sUE2XcAtSSBGJNl8JflLJI_BTp6N8P5HdGJEF-07003__mC0)
- #### Minh họa quy trình tự động tính lương và xử lý thanh toán vào ngày quy định.
- #### Mô tả nhiệm vụ và thuộc tính:
### PaymentProcessor:
- #### Nhiệm vụ: Tính lương, xử lý thanh toán.
- #### Thuộc tính: dateRange, paymentRecords.
### Employee:
- #### Nhiệm vụ: Cung cấp thông tin loại lương.
- #### Thuộc tính: employeeID, classification, paymentMethod.

## 4. Phân tích ca sử dụng: Maintain Timecard
### Các lớp phân tích:
- #### TimecardManager: Quản lý việc thêm, sửa, xóa timecard.
- #### Employee: Cung cấp thông tin nhân viên liên quan đến timecard.
- #### Project: Xác minh mã số dự án (charge number).
- #### PayrollDatabase: Lưu trữ dữ liệu timecard và thông tin dự án.
### Biểu đồ Sequence:
![PlanText](https://www.planttext.com/api/plantuml/png/b9HDRi8m48NtESKeAog52qIYGf1APK7L1LBNWps0MyUER8UAitNH8_KAjPqVIAWGzIAoxEVlpRoHylFrFRSEZQjBcI1psi1JMKbz8aegVooOg50vI3UY98Q6hr7XdamAQ66pN0z5htWoMie27MxHKXGLYv76w7TYBjw5VP9qXZ1z34Z8eOmcdUN4roMqoe2ZemmEkZRsJPiFuXcm0vezlTJbbin3Wj918uRP35BaF4t0hq3ry63dwKUK8g2M5sydGr1u561HEZ29Ls55sBGlEIhxozQmMFWRYyTpAzJskYhkQAUZUSpPY6cr4wR4qENGpqlwA7DmhINu58Y3hHaZQtUrbAVuZAGb4Eh-3bljBKyoHfjyH0LrnfBYIJI-c19nuGPZYgdjoVMXTQsiYYQJGHwT2ZWv5D9UaUeg1Fq7B0D5dqKSWjyyXpd4tV9g2BS7S2lyqDmu_N40d2GvkewWERylXNyLrO37LVdHpFqd_0X-0G00__y30000)
- #### Minh họa quy trình thêm hoặc sửa timecard.
- #### Mô tả nhiệm vụ và thuộc tính:
### TimecardManager:
- #### Nhiệm vụ: Xử lý logic ghi nhận thời gian làm việc.
- #### Thuộc tính: timecardID, hoursWorked, chargeNumber.
### Employee:
- #### Nhiệm vụ: Xác định nhân viên thực hiện timecard.
- #### Thuộc tính: employeeID, name.

## 5. Hợp nhất kết quả phân tích
### Tổng quan: 
### Hệ thống Payroll được phân tích dựa trên hai ca sử dụng chính:
- #### Payment: Tính lương và xử lý thanh toán tự động cho nhân viên theo các quy định.
- #### Maintain Timecard: Quản lý việc ghi nhận và lưu trữ thông tin giờ làm việc (timecard).
### Biểu dồ Sequence
![PlanText](https://www.planttext.com/api/plantuml/png/b5N1Yjim4BthAqHE2MH_83JBTkD2z-1YbeMUPwL9ubQMZ2HloRVrq4_gBtH6jcCx3Y4r11pDc_TctaZotzz_da847vlA253HUVcbgeqx8NP_2pXvPyndNPMs3D43BOgQCafLrc2ZNBoL5IhmEWSB1_GB2K6-xV8fY6WgjB7mJc48haKLnGp4MXb4U8U02PCzNs2y-u4gjldqVbKcntXqkiNaGcotCeVIHlh9lbgvtOg-LVdmo1NBZQnI3prcIHQKpgwbXeXhUNID3z-T_ubwBTKH_06_DTKx-fK04sKB9bwv0AqNGjB3h4JEXHBx1vYIgNQZtEMKY9EOB44d8Yd4Jo9xE9USaETW9vWzKoJ0nz0AThs-P7UqqxCHpI2adDsNlWBkSgf7aBEL6nbxXya5r38qYaU-RumvfJGq0MLfx--mmzxIHE-TtromIZlGejKY2O-cXBgCap4brmuOpwRrhRnahISJFyuxIIFjB1DcJ4tDHbyXMqkBlx8q17hvodD8RxlP46uFu9RvtDob-vS6Q3GOSMv1ktwV2_zLL4jyMHMDXezeTtRvO5wxTD8vAeZDDxQBBzdVLx07N0aAZIROYuVbIdJbfbn3R9_wuACmpjLoJzm8wZZSV6aF9hvH4mgCQWm9alXOcC73HT8BrN3AHjkYPIlOiBgz0hjkbmEmfIhoWMJcxQX9FjmTnoigHsCQCx6d36QcQrwc0dcPDAXs7efueYJ-3Fm3003__mC0)
### Hành vi qua biểu đồ Sequence
### 1. Payment
### Tóm tắt hành vi:
- #### PaymentProcessor khởi động quy trình vào ngày thanh toán.
- #### Lấy danh sách nhân viên từ PayrollDatabase.
- #### Dựa vào loại nhân viên:
- #### Tính lương (giờ công, cố định, hoa hồng).
- #### Tạo bản ghi thanh toán và gửi qua PaymentMethod.
- #### Cập nhật trạng thái thanh toán trong cơ sở dữ liệu.
### 2. Maintain Timecard
### Tóm tắt hành vi:
- #### Nhân viên nhập thông tin timecard qua giao diện.
- #### TimecardManager kiểm tra tính hợp lệ của dữ liệu (mã dự án, số giờ).
- #### Thông tin được lưu trữ vào PayrollDatabase.
- #### Nếu cần chỉnh sửa, TimecardManager tìm kiếm và cập nhật timecard tương ứng.
