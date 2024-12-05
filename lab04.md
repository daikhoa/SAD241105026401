# Thiết kế các ca sử dụng hệ thống Payroll System

## I. Danh sách các ca sử dụng chính
- **Đăng nhập vào hệ thống (User Login)**
- **Quản lý thông tin nhân viên (Manage Employee Information)**
- **Quản lý bảng chấm công (Manage Timecard)**
- **Tính toán bảng lương (Process Payroll)**
- **Xử lý thanh toán ngân hàng (Handle Bank Payments)**
- **In phiếu lương (Generate and Print Paychecks)**

## 1. Mô tả và giải thích các ca sử dụng

### 1.1. Đăng nhập vào hệ thống (User Login)
- ** tham gia**: Nhân viên, Quản trị viên hệ thống.

#### Dòng chảy chính
1. Người dùng nhập tên đăng nhập và mật khẩu.
2. Hệ thống kiểm tra tính hợp lệ của thông tin.
3. Nếu thông tin hợp lệ, hệ thống cho phép truy cập vào hệ thống.

#### Dòng chảy thay thế
- Nếu thông tin không hợp lệ, hệ thống hiển thị thông báo lỗi và yêu cầu người dùng nhập lại.

#### Biểu đồ tuần tự:
![diargam](https://www.planttext.com/api/plantuml/png/X50nJWCn4Ept5QFh-K0Ab1SW9894Qup5MV7vJlOQwUeKgQbeSwA84ea2YIfNK3WVkHVm1Uox0EbmOS_kpipk-gl_d7iMZaDbI4Yk7OfRhrm1uH4Ie2OLjTIDi8pYMhIkDWOthMTLZIG_Gg9CniNbASOCL-LmU6l0SMznV3wkx2Fib7gA6rG9CPOfiGjqqfohxs8dmUNGl-SdVYGrQql2C1Q_8LBzjO4P-ZKXdJ-VSPeP5YwqaDCSPTpO4Z9hIHclpdsM4_pNRgBTnwxEh1SzhjB6VSXDjk5dGJCSEatAFj0yNUbhlm400F__0m00)

#### Lý do thiết kế:
- Đảm bảo chỉ người dùng hợp lệ có quyền truy cập hệ thống, tăng cường bảo mật.
- Giảm nguy cơ truy cập trái phép và bảo vệ dữ liệu quan trọng.

### 1.2. Quản lý thông tin nhân viên (Manage Employee Information)
- **tham gia**: Quản trị viên hệ thống.

#### Dòng chảy chính
1. Quản trị viên thêm hoặc chỉnh sửa thông tin nhân viên (tên, địa chỉ, lương cơ bản, v.v.).
2. Hệ thống xác nhận và cập nhật cơ sở dữ liệu.

#### Dòng chảy thay thế
- Nếu dữ liệu không hợp lệ, hệ thống thông báo lỗi và yêu cầu điều chỉnh thông tin.

#### Biểu đồ tuần tự:
![diargam](https://www.planttext.com/api/plantuml/png/T56nQiCm4Dtr5G_lfNk6ajAnIw7z0LKsbQWi6qiEUEuG-WKPaxH3mM2wT8g63eB-XxwWlz2Jau09gORJSVVUktVIh_-UMySRrvQQSU6g1jbrNYgJWLlmbB6QsagecXk7x8vtJQKrxZlhYd94sJ5bR4JZukfGm0mFClJbfP3Hlne96_t0uMJuCazm13Kol1aiLEWDEt2cx5iL_Ki9rn0f32H0EkyrTFHBnhLBwaUbIGTqpeZTnDrGqqIw71PXKq7yR9EbDVBeFw5fsB8zOUytcXqdFOPjbVnlo8j85LPeMqnzFE_JV-sS4oJOIYLBw4BVGiJT1yNfcx72v6nEWJxf3m00__y30000)

#### Lý do thiết kế:
- Hệ thống cần lưu trữ và quản lý thông tin nhân viên để phục vụ quá trình tính lương.
- Đảm bảo thông tin nhân viên luôn được cập nhật chính xác và kịp thời.

### 1.3. Quản lý bảng chấm công (Manage Timecard)
- **tham gia**: Nhân viên.

#### Dòng chảy chính
1. Nhân viên nhập mã chi phí và số giờ làm việc hàng ngày.
2. Hệ thống kiểm tra thông tin và cập nhật bảng chấm công vào cơ sở dữ liệu.

#### Dòng chảy thay thế
- Nếu nhập sai mã chi phí hoặc số giờ, hệ thống sẽ báo lỗi và yêu cầu nhập lại.

#### Biểu đồ tuần tự:
![diargam](https://www.planttext.com/api/plantuml/png/T56zIWGn6Epp5CFsli0LSY1MWWZw0hbSk0IJRDXa3xQsiBxAIjXZ4K7OpcgtiCYJv0by1RC_9ujuAS9y-MRccoJV_TVQULhuKYj2cSyBPDVQghpYF0Dru7D1R2999Yqr7jaThOfSATnNpdCz4jq82Ja9S74vds65Mn6xraA71an8M15Qx4CD5_i3TZBshr2XrjWd-Cp8h5iwtAJEauOlA7neZO28VMEX4fzGvV4WmgVPmKkpx22jVyoknZHc2EMnYLsJb2nLRnfiiFcZ-xtIwZHc4uuvl0Xr2Z8fk79y6U9nWcUpdF5Cp1SvFaqLFagmsBsNKz31fJjAmisMhDEMFkm7003__mC0)

#### Lý do thiết kế:
- Quản lý thời gian làm việc của nhân viên là cơ sở quan trọng để tính lương chính xác.
- Đảm bảo dữ liệu về giờ làm việc được lưu trữ và quản lý đầy đủ.

### 1.4. Tính toán bảng lương (Process Payroll)
- ** tham gia**: Quản trị viên hệ thống lương.

#### Dòng chảy chính
1. Hệ thống lấy dữ liệu từ bảng chấm công và thông tin nhân viên để tính lương.
2. Hệ thống tự động tính toán số tiền lương dựa trên giờ làm việc, mức lương và các khoản phụ cấp.
3. Kết quả tính toán lương được ghi vào hệ thống và chuẩn bị gửi đi thanh toán.

#### Dòng chảy thay thế
- Nếu có lỗi dữ liệu từ bảng chấm công, hệ thống thông báo lỗi và yêu cầu chỉnh sửa.

#### Biểu đồ tuần tự:
![diargam](https://www.planttext.com/api/plantuml/png/R94nJiGm44Nxd6AqFHUWGBjegQ108XTm4cjjaOo3Cq7a1DIKL6n0D0Z45bH9iOLHxk4JS0KSRxJP81fhD7v__X_xfztE2sAQoYmDM4nAm-oILLgbAIoIJE8CM06ihuBSOJAMEKCQeQkg89vvgl3b50jbncEc4rWoOX4hk2Tfw2vFf_HPbgUgudnAyw7hwC0dWQEJmGoEuLpOzad2zuDj7t45DwMfWRHvHm5aFjoPTfkknbKmA9nsj7VwK9SLt9MsUIL8RFi9gRJjVGcHRLxSl5YucmnYypKPCMRwCu94JpeB11Jc6U5McZSyKEw3XpuTALFZFndts4MtAU7QDbjokxbCmrPUTy3l7iPDtVb7fbOWb5bZdsYD8fXpJFfF_WK00F__0m00)

#### Lý do thiết kế:
- Hệ thống hóa quá trình tính lương giúp giảm thiểu sai sót và tiết kiệm thời gian.
- Đảm bảo tính chính xác trong việc tính lương cho nhiều loại hình nhân viên.

### 1.5. Xử lý thanh toán ngân hàng (Handle Bank Payments)
- **tham gia**: Quản trị viên hệ thống lương.

#### Dòng chảy chính
1. Hệ thống gửi yêu cầu thanh toán đến ngân hàng thông qua giao diện kết nối ngân hàng.
2. Ngân hàng phản hồi xác nhận giao dịch thành công.

#### Dòng chảy thay thế
- Nếu có lỗi trong giao dịch, hệ thống lưu lỗi vào nhật ký và thông báo cho quản trị viên.

#### Biểu đồ tuần tự:
![diargam](https://www.planttext.com/api/plantuml/png/Z94nJiCm58Ptd-9NToxG0HKMLYGOM1qdggqwTfMy8EKC7A1hCrH8IDsO4Y46dyGdu0hOJaNIme07wptfU___F_jh-5pLn2jgIisu85jXSS_RocgDcxnKPW5UWyUARGEcXDfoGnFqqDPKb8cgKtcEtNApcJDPw1bBUhYwFerWYJi_71LQzzP0-Fwr0Kbk9CYwph0J5VWu_aEJTEzc3GfISvfhmkFKHsmV6X5XXd2IoDpyoNK2Hlh-QB1Mt2BtmukGloUd8EC6os2KCcIki-TueUlY8eRl3uJCzvtwEyPSI_jXfouyfyUIQWJmxFPsJ4xOk8z_X1o52vEpLRZYhty3003__mC0)

#### Lý do thiết kế:
- Hệ thống cần tích hợp với ngân hàng để thực hiện thanh toán nhanh chóng và chính xác.
- Quản lý và ghi nhận lỗi giúp khắc phục kịp thời những vấn đề phát sinh.

### 1.6. In phiếu lương (Generate and Print Paychecks)
- **tham gia**: Quản trị viên hệ thống lương.

#### Dòng chảy chính
1. Hệ thống tạo phiếu lương cho từng nhân viên.
2. Gửi lệnh in tới máy in thông qua giao diện dịch vụ in.

#### Dòng chảy thay thế
- Nếu không tìm thấy máy in, hệ thống sẽ báo lỗi và yêu cầu kiểm tra kết nối.

### Biểu đồ tuần tự
![diargam](https://www.planttext.com/api/plantuml/png/V96nIWGn48RxFCLmlIzW8MSb5e9mDfOn6ynmsMn8ii8-WRMLhOk880WMLhl55O5xZpo1h-0ahjno1vSY6MQ-V_uPyZDkbZvm5zfQCov2us1npJlNQ0tdLOrc0Tm3pn6pXA50oqtOGQlE1raNofTm3tD8pqgw1nIoK3Pdf6EiD8MJiqa7ft0RFreGQNXlWIfMOHesBUZjrxOtzsp2veARDFGDX3G-sYFuv4ZyHHe_4JJnHf45uph0LUoxRBTMQNY5Aerl90Ow_xAvuQM1eE8BgKNydhYTqTz6D9RAHRYBD1pkAQJsSkPPm0Fhuorf_cU4DMqRmAJn2Paq5LlIbJ_n5m00__y30000)

#### Lý do thiết kế:
- **Tạo phiếu lương minh bạch**: Đảm bảo mỗi nhân viên nhận được phiếu lương chi tiết và rõ ràng.
- **Tích hợp với hệ thống in**: Giảm thiểu sai sót và sự cố trong quá trình in ấn phiếu lương.









ChatGPT có thể 
