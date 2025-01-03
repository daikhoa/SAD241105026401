# A wilderness weather station
## I.Mô tả tóm tắt bài toán:
### 1.Mục tiêu của bài toán:
Xây dựng hệ thống trạm thời tiết tự động hoạt động trong các khu vực vùng sâu, vùng xa, không có cơ sở hạ tầng hỗ trợ (điện, đường giao thông, mạng viễn thông). Hệ thống này có nhiệm vụ thu thập, xử lý và truyền dữ liệu thời tiết về trung tâm để phục vụ:
- Nghiên cứu và phân tích biến đổi khí hậu ở cả cấp địa phương và quốc gia.
- Nâng cao độ chính xác của dự báo thời tiết quốc gia.
- Hỗ trợ quản lý tài nguyên thiên nhiên và phòng chống thiên tai.
### 2.Các đặc điểm chính của hệ thống:
#### 2.1.Tự cấp nguồn năng lượng:
- Sử dụng năng lượng tái tạo (năng lượng mặt trời hoặc gió) để vận hành toàn bộ hệ thống, không phụ thuộc vào nguồn điện bên ngoài.
#### 2.2.Giao tiếp từ xa qua vệ tinh:
- Truyền dữ liệu thời tiết về hệ thống trung tâm và nhận cập nhật phần mềm hoặc cấu hình từ xa.
#### 2.3.Hoạt động tự động và đáng tin cậy:
- Hệ thống phải hoạt động độc lập trong thời gian dài, có khả năng tự xử lý lỗi cơ bản và tự khởi động lại khi cần.
#### 2.4.Tự cấu hình và nâng cấp từ xa:
- Cho phép thay đổi cấu hình hoặc cập nhật phần mềm từ xa mà không cần truy cập trực tiếp.
### 3.Sự cần thiết và lợi ích khi giải quyết bài toán:
Trạm thời tiết vùng hoang dã là một thành phần quan trọng trong hệ thống thu thập thông tin thời tiết quốc gia. Việc xây dựng và triển khai trạm thời tiết tự động ở những khu vực không có cơ sở hạ tầng (điện, mạng, đường xá, v.v.) mang lại những lợi ích sau:
- Hỗ trợ nghiên cứu biến đổi khí hậu: Dữ liệu từ các trạm thời tiết giúp phân tích biến đổi khí hậu cục bộ và quốc gia, hỗ trợ các nhà khoa học đưa ra các dự báo chính xác hơn về xu hướng thời tiết trong tương lai.
- Cung cấp thông tin dự báo thời tiết: Các trạm này đóng góp vào hệ thống dự báo thời tiết quốc gia, phục vụ cho các hoạt động dự báo và cảnh báo sớm, đặc biệt là trong những tình huống thiên tai như bão, lũ lụt, hay hạn hán.
- Quản lý tài nguyên tự nhiên và giảm thiểu rủi ro thiên tai: Dữ liệu thời tiết có thể giúp các nhà khoa học và cơ quan chính phủ quản lý nguồn tài nguyên hiệu quả và phản ứng nhanh với các sự kiện thời tiết cực đoan.
### 4.Các yêu cầu chức năng:
#### 4.1.Thu thập và xử lý dữ liệu thời tiết:
- Trạm cần có khả năng đo và lưu trữ các thông số thời tiết như nhiệt độ, độ ẩm, áp suất không khí, tốc độ và hướng gió, lượng mưa.
- Dữ liệu phải được xử lý sơ bộ trước khi gửi về hệ thống trung tâm qua vệ tinh.
#### 4.2.Lưu trữ và xử lý dữ liệu:
- Hệ thống cần khả năng lưu trữ dữ liệu thu thập được trong bộ nhớ tạm thời, và sau đó gửi dữ liệu này lên hệ thống trung tâm khi có kết nối.
#### 4.3.Kết nối và truyền tải dữ liệu:
- Khi có tín hiệu vệ tinh hoặc mạng không dây, trạm cần có khả năng truyền tải dữ liệu về trung tâm để phân tích và sử dụng cho các mục đích dự báo.
#### 4.4.Quản lý năng lượng:
- Trạm cần có khả năng tự tạo điện năng từ nguồn năng lượng tái tạo như tấm pin mặt trời hoặc năng lượng gió và có hệ thống quản lý năng lượng hiệu quả để đảm bảo hoạt động liên tục.
#### 4.5.Khả năng tự động điều chỉnh và cấu hình lại:
- Hệ thống phần mềm cần có khả năng tự cấu hình lại để đối phó với các lỗi thiết bị, thay đổi trong môi trường, hoặc nâng cấp phần mềm từ xa.
#### 4.6.Bảo mật và độ tin cậy:
- Đảm bảo rằng dữ liệu được thu thập và truyền tải một cách an toàn, không bị tấn công hoặc giả mạo.
### 5.Các Yêu Cầu Phi Chức Năng:
Các yêu cầu phi chức năng cho hệ thống trạm thời tiết hoang dã chủ yếu tập trung vào khả năng hoạt động độc lập và tính bền vững của hệ thống:
#### 5.1.Tính độc lập và tự chủ:
- Vì các trạm thời tiết được triển khai ở những khu vực xa xôi, không có cơ sở hạ tầng, hệ thống phải hoạt động hoàn toàn độc lập. Điều này bao gồm tự cung cấp năng lượng, tự duy trì và tự khởi động lại sau sự cố.
#### 5.2.Khả năng chống chịu môi trường khắc nghiệt:
- Trạm cần phải có thiết kế bền vững để chịu được các điều kiện môi trường khắc nghiệt như gió mạnh, mưa lớn, nhiệt độ cực đoan, và các yếu tố tự nhiên khác.
#### 5.3.Tiết kiệm năng lượng:
- Với nguồn năng lượng hạn chế từ năng lượng tái tạo, trạm phải có khả năng tối ưu hóa việc sử dụng năng lượng để duy trì hoạt động liên tục trong điều kiện ít ánh sáng mặt trời hoặc gió
#### 5.4.Khả năng mở rộng:
- Hệ thống cần có khả năng dễ dàng mở rộng và thêm mới các trạm thời tiết mà không cần thay đổi cấu trúc hoặc phần mềm hệ thống hiện tại.
#### 5.5.Bảo trì và sửa chữa dễ dàng:
- Dù khó tiếp cận, nhưng hệ thống phần cứng và phần mềm của trạm cần phải thiết kế sao cho dễ bảo trì và sửa chữa từ xa, chẳng hạn như khả năng tự chẩn đoán sự cố và cập nhật phần mềm từ xa.

## II.Phân tích các ca sử dụng:
### 1. Kiến trúc đề xuất:
Hệ thống được thiết kế theo kiến trúc hướng đối tượng (object-oriented architecture) với các thành phần chính sau:
- Lớp cảm biến (Sensors):
  - Thu thập dữ liệu thời tiết từ các cảm biến như nhiệt độ, độ ẩm, tốc độ gió, áp suất không khí, lượng mưa.
  - Gửi dữ liệu thô đến lớp xử lý.

- Lớp xử lý dữ liệu (Data Processor):
  - Xử lý dữ liệu thô từ cảm biến, bao gồm làm sạch dữ liệu, phát hiện lỗi, và chuẩn bị dữ liệu để gửi đi.
  - Phân loại và lưu trữ dữ liệu tạm thời trong bộ nhớ.

- Lớp quản lý năng lượng (Power Management):
  - Theo dõi và quản lý việc tiêu thụ năng lượng của hệ thống.
  - Điều phối hoạt động của các thành phần dựa trên mức năng lượng hiện có từ nguồn tái tạo.

- Lớp truyền thông (Communication):
  - Kết nối với hệ thống vệ tinh để truyền dữ liệu về trung tâm.
  - Nhận lệnh hoặc bản cập nhật phần mềm từ trung tâm.

- Lớp quản lý lỗi (Fault Management):
  - Phát hiện lỗi phần cứng hoặc phần mềm và kích hoạt cơ chế khắc phục (tự cấu hình lại hoặc thông báo lỗi).

- Lớp điều khiển chính (Main Controller):
  - Điều phối hoạt động của các lớp trên, đảm bảo hệ thống hoạt động liên tục và chính xác.

### Biểu đồ kiến trúc đơn giản:
![Login](https://www.planttext.com/plantuml/png/ZLGzRnD14ErFklymFR54xG854X4X9SWeAMZNvvDlbTjPixSB14GHKQIWmK88KL0aLgeeIb12SokKugpyZ_qdxAxlOj-79LoSvDityzxCUtkRcIH2AfQ6GNP8SK84OH2b9CkUIYdeKCduHSHndtw8uN4OX84_Wpr2SOkZ53nDOm4Vmm3ixn7ClrAZZnLC4gEd519kybC9ywdHFt6y19bync1ednoC_euUy0KJi5Kd85sjGtzQykt7c76HxPAZLRQ3H3bqVZc1aT5Na5ho4_zA_w8WgSdlP8NTCVgIDc35hMFExn2sYIG3mQCuipIUfKRVFbwAU6qRGrhyRVMk08Eai3j8t052QlGFMftitbzRg71rqYwAbShNItvVSPMojpXZ2cb49ENObZtWxsAnHv2COnQZR6qlvZ0g_b30-MSSGtf_RVHiQPFLVOQLazqGg_0RwyE1oSyPJ2XkW5IaDwG8OrhSRBXNhgOSigQjBNr5cL17DaPOc_sD8l3MvuDYKY5VElSH8fy1T7-aNQM-i8JAwfN56QknFYSgbMitiaCBQqBcxF8-DV9OYZFwDnnQggl8B-SygfkwS6rOd7A8t6FHoIe_RejgNADUxqazwVt6XUgiw0ZdVzLrfgCFhvIzb-XJrZIzeqc7ZKroD_R2JdShrlJfDARLwI7_vSR3eBQkjTlORbtD3jZQSLQhvzDYzY0Z33fbkqQD4Vlmh1u8ftqpnf7_ylu3)


### 2.Các cơ chế phân tích:
#### 2.1.Cơ chế làm sạch dữ liệu (Data Cleaning): Làm sạch dữ liệu thu thập từ các cảm biến, loại bỏ các giá trị nhiễu hoặc không hợp lệ.
##### Phân tích cơ chế:
- Các cảm biến thu thập dữ liệu có thể gặp sự cố hoặc bị nhiễu do môi trường (ví dụ: cảm biến nhiệt độ bị ảnh hưởng bởi ánh sáng mặt trời trực tiếp hoặc cảm biến gió bị ảnh hưởng bởi các vật cản).
- Data Cleaning đảm bảo rằng dữ liệu đầu vào là chính xác và có thể sử dụng cho các phân tích sau này.
- Lợi ích: Giúp đảm bảo chất lượng dữ liệu đầu vào, từ đó cải thiện độ chính xác của dự báo thời tiết và các nghiên cứu về biến đổi khí hậu.
##### Các hoạt động chính:
- Loại bỏ các giá trị cực trị hoặc không hợp lý (ví dụ: nhiệt độ cực cao hoặc thấp).
- Chuẩn hóa dữ liệu từ các cảm biến khác nhau (ví dụ: chuyển đổi đơn vị đo lường nếu cần).

#### 2.2.Cơ chế phát hiện lỗi (Error Detection): Phát hiện các lỗi phần cứng hoặc lỗi dữ liệu bất thường trong hệ thống.
##### Phân tích cơ chế:
-Trạm thời tiết làm việc trong môi trường khắc nghiệt và xa xôi, vì vậy việc phát hiện lỗi kịp thời là rất quan trọng.
- Error Detection đảm bảo hệ thống có thể xác định các vấn đề như:
    - Lỗi phần cứng (ví dụ: cảm biến không hoạt động).
    - Dữ liệu bất thường hoặc bị lỗi (ví dụ: cảm biến bị hỏng hoặc gặp sự cố truyền thông).
- Lợi ích: Phát hiện lỗi sớm sẽ giúp tiết kiệm thời gian và chi phí sửa chữa, đồng thời duy trì tính ổn định của hệ thống.
##### Các hoạt động chính:
- Giám sát trạng thái các cảm biến và các thành phần hệ thống.
- So sánh dữ liệu thu thập được với các mô hình dự đoán (như mô hình khí hậu cơ bản) để phát hiện sự bất thường.

#### 2.3.Cơ chế giám sát năng lượng (Energy Monitoring): Theo dõi và quản lý mức năng lượng sử dụng của hệ thống.
##### Phân tích cơ chế:
- Trạm thời tiết cần hoạt động hoàn toàn tự động và không phụ thuộc vào nguồn năng lượng từ bên ngoài. Do đó, Energy Monitoring đóng vai trò quan trọng trong việc đảm bảo nguồn năng lượng luôn đủ để duy trì hoạt động của các cảm biến, bộ xử lý và hệ thống truyền thông.
- Lợi ích: Đảm bảo rằng hệ thống có đủ năng lượng để hoạt động liên tục, đặc biệt trong các điều kiện khắc nghiệt (ví dụ: thời tiết xấu, không có ánh sáng mặt trời).
- Các yếu tố năng lượng như tấm pin mặt trời, tua-bin gió và pin lưu trữ phải được theo dõi và điều phối để tối ưu hóa hiệu suất.
##### Các hoạt động chính:
- Theo dõi mức năng lượng từ các nguồn cung cấp (năng lượng mặt trời, gió, pin).
- Ước tính mức tiêu thụ năng lượng và cảnh báo khi mức năng lượng giảm xuống dưới ngưỡng tối thiểu.

#### 2.4.Cơ chế tự động cấu hình lại (Auto Reconfiguration): Khôi phục hoạt động của hệ thống khi phát hiện lỗi nhỏ hoặc sự cố.
##### Phân tích cơ chế:
- Hệ thống trạm thời tiết hoạt động ở những khu vực xa xôi, khó tiếp cận, do đó, việc sửa chữa hoặc can thiệp trực tiếp sẽ rất khó khăn.
- Auto Reconfiguration giúp hệ thống tự động khôi phục hoặc tái cấu hình khi gặp sự cố nhỏ (ví dụ: cảm biến bị hỏng, hoặc phần mềm gặp lỗi).
- Lợi ích: Tiết kiệm chi phí và thời gian, duy trì hoạt động của hệ thống mà không cần phải sửa chữa trực tiếp.
##### Các hoạt động chính:
- Cấu hình lại các thành phần hệ thống khi phát hiện lỗi nhỏ.
- Khởi động lại các cảm biến hoặc bộ phận bị lỗi mà không cần can thiệp từ xa.

#### 2.5.Cơ chế truyền thông qua vệ tinh (Satellite Communication): Đảm bảo việc truyền tải dữ liệu từ hệ thống trạm thời tiết đến trung tâm điều hành và nhận cập nhật từ trung tâm.
##### Phân tích cơ chế:
- Hệ thống cần truyền tải dữ liệu thời tiết thu thập được đến các trung tâm điều hành qua vệ tinh, vì khu vực lắp đặt không có cơ sở hạ tầng truyền thông.
- Satellite Communication cung cấp kênh truyền thông cần thiết cho hệ thống, giúp dữ liệu được truyền tải an toàn và hiệu quả.
- Lợi ích: Giúp hệ thống duy trì kết nối liên tục dù ở khu vực xa xôi, giúp cập nhật thông tin kịp thời và nhận các bản cập nhật hoặc lệnh từ trung tâm.
##### Các hoạt động chính:
- Truyền dữ liệu thu thập về trung tâm.
- Nhận các lệnh hoặc bản cập nhật phần mềm từ trung tâm.

#### 2.6.Cơ chế lưu trữ tạm thời (Temporary Storage): Lưu trữ tạm thời dữ liệu trước khi xử lý hoặc gửi đi.
##### Phân tích cơ chế:
- Dữ liệu từ các cảm biến cần được lưu trữ tạm thời để xử lý trước khi gửi đi hoặc khi cần thực hiện các phép tính phân tích.
- Temporary Storage giúp lưu trữ và giữ dữ liệu an toàn cho đến khi được xử lý hoặc truyền đi.
- Lợi ích: Đảm bảo rằng dữ liệu không bị mất trong trường hợp có sự cố và có thể được truy xuất lại khi cần thiết.
##### Các hoạt động chính:
- Lưu trữ dữ liệu trong bộ nhớ tạm thời trước khi gửi đi.
- Quản lý dung lượng bộ nhớ để tối ưu hóa việc lưu trữ.

### Biểu đồ quan hệ của các cơ chế:
![Login](https://www.planttext.com/plantuml/png/VLJBRjD05DrRyZ_SFQh4EWlKaY90F8H85smdpk0PrPunanc9WbXLA0iM9Ik4K0MXYX2Fg4M8ZKU8XQFyn_m9Tvn7FKbA5exjkVUSUyyvoMvV4wLDdiLH_v2BWYYIGvAHVdzFQyMxHjExYHGT_eB2zJYAe_eCzeacxOmImKKAB-C8y7CDxajNZZXqdJs1dhFda75d1mO4m-_NPbdMPiQLNmMmwXTfriNHgqk6Mqf9jKyrJJINufBZ4Qj66ZpWG43cx3iEYIlFSkXoL_uL_obhJjHrvLY3PhCBPqz56Z8BgjAZ1r9mBLMmtm6Z4dhLRmvYUem7cMy_mvi5Z_RhBujdvyv-I41N4y7MwpMllXcaTtOSKEyPBHzJrFifJuqYuUO7plw4wT3PzuY0EuyDAlW3mRDQTGGRr913F3vaVB6rm3SdIuXx-F2Hhq3cZPfLdn2bOAxy8hnvR-QjmMGTeccMSKtRCi-DuCdQSBUTdOGI8mdw0LePlt3rEL-MFaIYYV0RJ0e_NZb19vpz7fGsg0zeNaX5r547_I0fRUHjTc42Jcz0NejmklBX3kw2q2WyF3FL26zhqPxZm91LVxO4C0ZtpiwDzIosuCcoMIjlAThi1IysCXT7QwqURPl9BRXPZUJ2Cc_FyQR32BQUpAlXfc_dFmgyoetqAOdNfXXRkAumt3Dk6DBQuaHJcBGEntI8i1kz7Z0Gl0LjimXu4K0cJAvSypRjKj6h_xZ-0G00)

### 3.Kết quả các ca phân tích:
#### Ca sử dụng 1: Thu thập dữ liệu thời tiết
##### Mục tiêu: Thu thập dữ liệu về các yếu tố khí hậu (nhiệt độ, độ ẩm, áp suất không khí, tốc độ gió) từ các cảm biến trong khu vực.
- Mô tả:
  - Người tham gia: Cảm biến (sensors), hệ thống giám sát.
- Tiến trình:
  - Cảm biến đo lường các yếu tố khí hậu.
  - Dữ liệu thu thập được sẽ được chuyển tiếp đến DataProcessorLayer để làm sạch và xử lý.
- Kết quả: Dữ liệu thời tiết chính xác được thu thập và chuyển đến lớp xử lý.

#### Ca sử dụng 2: Xử lý dữ liệu và phát hiện lỗi
##### Mục tiêu: Xử lý dữ liệu thu thập được từ các cảm biến, đồng thời phát hiện lỗi trong quá trình thu thập.
- Mô tả:
  - Người tham gia: DataProcessorLayer, ErrorDetection.
- Tiến trình:
  - Dữ liệu thô được gửi đến DataProcessorLayer để làm sạch và xử lý.
  - ErrorDetection phát hiện lỗi dữ liệu hoặc phần cứng.
  - Nếu phát hiện lỗi, hệ thống sẽ gửi cảnh báo về FaultManagementLayer.
- Kết quả: Dữ liệu được xử lý và lỗi (nếu có) sẽ được phát hiện và báo cáo.
  
#### Ca sử dụng 3: Quản lý năng lượng
##### Mục tiêu: Quản lý nguồn năng lượng của hệ thống để đảm bảo hoạt động liên tục.
- Mô tả:
  - Người tham gia: PowerManagementLayer.
- Tiến trình:
  - EnergyMonitoring theo dõi tình trạng năng lượng của hệ thống.
  - Kiểm tra mức năng lượng từ các nguồn (pin mặt trời, tua-bin gió, pin lưu trữ).
  - Nếu mức năng lượng quá thấp, hệ thống sẽ kích hoạt chế độ tiết kiệm năng lượng hoặc gửi cảnh báo về trung tâm.
-Kết quả: Đảm bảo hệ thống luôn có đủ năng lượng hoạt động và không bị gián đoạn.

#### Ca sử dụng 4: Truyền tải dữ liệu qua vệ tinh
##### Mục tiêu: Truyền tải dữ liệu về trung tâm điều khiển để phân tích và lưu trữ.
- Mô tả:
  - Người tham gia: CommunicationLayer, SatelliteCommunication.
- Tiến trình:
  - Dữ liệu đã được xử lý sẽ được gửi qua vệ tinh đến trung tâm điều khiển.
  - Dữ liệu có thể là các thông tin thời tiết, báo cáo sự cố hoặc cập nhật từ hệ thống.
  - Trung tâm điều khiển sẽ nhận dữ liệu và đưa ra quyết định dựa trên thông tin nhận được.
- Kết quả: Dữ liệu được truyền đi thành công, đảm bảo việc theo dõi và phân tích từ xa.

#### Ca sử dụng 5: Phát hiện và xử lý lỗi tự động
##### Mục tiêu: Phát hiện lỗi trong hệ thống và tự động tái cấu hình để tiếp tục hoạt động.
- Mô tả:
  - Người tham gia: FaultManagementLayer, AutoReconfiguration.
- Tiến trình:
  - FaultManagementLayer giám sát và phát hiện các lỗi hệ thống (cảm biến không hoạt động, mất kết nối, lỗi dữ liệu).
  - AutoReconfiguration tự động khôi phục hệ thống khi có lỗi nhỏ, chẳng hạn như tái khởi động lại cảm biến hoặc hệ thống.
  - Nếu lỗi không thể tự động xử lý, hệ thống sẽ gửi cảnh báo về trung tâm điều khiển.
- Kết quả: Hệ thống khôi phục hoạt động hoặc cảnh báo về lỗi nghiêm trọng.

#### Ca sử dụng 6: Lưu trữ tạm thời dữ liệu
##### Mục tiêu: Lưu trữ dữ liệu tạm thời trước khi xử lý hoặc truyền tải.
- Mô tả:
  - Người tham gia: TemporaryStorage, DataCleaning.
- Tiến trình:
  - Dữ liệu thu thập được từ cảm biến được lưu trữ tạm thời trong bộ nhớ.
  - Sau đó, dữ liệu này sẽ được xử lý bởi DataCleaning và ErrorDetection để làm sạch và phát hiện lỗi.
- Kết quả: Dữ liệu được lưu trữ an toàn và có thể truy xuất lại khi cần thiết.

### Biểu đồ kết quả các ca sử dụng:
![Login](https://www.planttext.com/plantuml/png/ZLJ1RjD04Br7oZ-CUk-1j6ah3gZ2792Agg0cWglZM5chphhOkuKUKG-vaXFYW4HQ8GvjHP4uUOKuEEf_x9ymit7YtIIkk3Yoi-_DU_DczZ0JVYhaA6us_40aAMnrKvrFHz1bMdsDe1lf_A_O0Z-3Dw4lM9YU25z42RVEIpw4Rd4rWjcdIAkF4euO_bvoW_8IBj8aza8kmdG9ydH-FOBdH3u_TXBoBAd-VwdLs4YO8FVnx1AVhnxkjRhcGtEyaxn79HUP24VDHhCXip3min35C0c2wVpk30PQ_OGOXOpD9p8ZAZCzxua5UwlL7SJ57mTqNdo3CrPC1P2TCOTOgyzHYMvPwDSItN23vqPgR4ljUJksm5HUO8yu2CH4JhrtqeTpyYqYpahehWNjs5f8t8U5QYCC6TKlc4sq-hAitBRWs3ziH4e5XKcuR8ebeKJjRKPjzBPldJsYr94tzOsyFZfCyAsuXS34tQ_Yxda7b9ixKh2z_Oo2WQTGbwDMDmvP3KKBAPQPafRJIfh5LuFUGRJbHT12e7E1_OzMkb33q4Q6pjhe03FfpgUw1hc7oFz8YfhdR5O9tqNuCVLjFY53xC4ZGxQPerrneENVwBPVJ9FI0h5Y0DybiEAMC_oQJrUDDHlpRRRozEYE89oRfnkbjTHM4XRKxJq4B5cflCwmx_PpXM7mS6_0Dpwf9gdL_BnmTVxWrRvbleHJXXktd582jwm8ry6pYIaQKF6DwIv85rM8ibrI7hWJ-SXs6OhrMuli7OPyO2xwVm00)

## III.Xác định các phần tử thiết kế
### 1. Các phần tử thiết kế chính
**a. Các thành phần phần cứng (Hardware Components)**

**Cảm biến (Sensors):**

**Chức năng:**
- Thu thập dữ liệu môi trường như nhiệt độ, độ ẩm, áp suất không khí, tốc độ gió.
  
**Ví dụ:**
-  Cảm biến nhiệt độ (Thermometer), cảm biến độ ẩm (Hygrometer), cảm biến áp suất (Barometer).
  
**Bộ xử lý chính (Main Processor):**

**Chức năng:**
- Điều phối hoạt động của hệ thống, xử lý dữ liệu, thực thi các thuật toán phát hiện lỗi.
  
**Bộ nhớ tạm (Temporary Storage):**

**Chức năng:**
- Lưu trữ dữ liệu tạm thời trước khi xử lý hoặc truyền tải.
  
**Nguồn năng lượng (Power System):**

**Chức năng:**
- Cung cấp năng lượng, bao gồm tấm pin mặt trời, tua-bin gió và pin dự trữ.
  
**Hệ thống truyền thông vệ tinh (Satellite Communication Module):**

**Chức năng:**
-Truyền tải dữ liệu từ hệ thống tới trung tâm điều khiển từ xa.

**Mô hình hóa thành phần phần cứng:**

![Diagram](https://www.planttext.com/plantuml/png/V9DBReD038Rtd6AKLRF81LXKKTDANJHI9781bx78g8oDF8O8LJbP5prIhr0DZq0UBIl0zl_vjsT-lhxNGK6qzcLIGVu11Ph5AuWzWg3PiA-Oa3Gip6TYJ5v222P32YpTZ_XuX50BFeF2mp8Tel4hCUPqBjg2evrmZc5UcpEBTGIAMHiKVHHesDaXNFK5dRG5XRdwCZM37jeRsXvznGBIPieIFOt0e3oqskjTI5p21LKSDcTZVzDsV4Jf3KnJONBAqeNUiC6oa-WI5RGEPqX-02dm2LHHsYl_uUWqF-pvXL2ADeF6KR5bYxEqgOiC5ClIAMxO-vfS3kgOjcphSlAl0XIyqtz6yCvS8j3K8BgcqmIo4JoyTkp4ZATXjNgysd5g0f8D9b8ISnMCwJTBIllrX77lQCVY-OJlaIhXnjbO6HFlqluTpqMlfsIDPEED-0K00F__0m00)

**b. Các thành phần phần mềm (Software Components)**

**Bộ xử lý dữ liệu (DataProcessor):**

**Chức năng:**
- Xử lý dữ liệu thô từ các cảm biến, làm sạch dữ liệu và phát hiện các lỗi.
  
**Bộ phát hiện lỗi (ErrorDetectionModule):**

**Chức năng:**
- Phân tích dữ liệu để phát hiện bất thường hoặc lỗi hệ thống.
  
**Quản lý năng lượng (PowerManagementModule):**

**Chức năng:**
- Theo dõi và tối ưu hóa việc sử dụng năng lượng, chuyển hệ thống sang chế độ tiết kiệm năng lượng khi cần thiết.
  
**Quản lý lỗi (FaultManagementModule):**

**Chức năng:**
- Phát hiện và xử lý các lỗi trong hệ thống, kích hoạt cơ chế tự phục hồi (AutoReconfiguration).
  
**Bộ giao tiếp vệ tinh (SatelliteCommunication):**

**Chức năng:**
- Quản lý truyền tải dữ liệu qua vệ tinh tới trung tâm điều khiển.
  
**Hệ thống lưu trữ (StorageModule):**

**Chức năng:**
- Lưu trữ dữ liệu tạm thời hoặc dài hạn, đảm bảo dữ liệu không bị mất khi có sự cố.

  **Mô hình hóa thành phần phần mềm:**
  
  ![Diagram](https://www.planttext.com/plantuml/png/Z5DBJiD03Dtd51QhTi45Pe4gyLc1L54uW9anOKGoZcod5KKz6GkEn1NG9A6q9Qt8Ad7UP_pi-VhudAcXM5jNHOF-5Kk2imK_smg5u9BhXXCbqpDuBm1yXQfmXOPpOK-gB5qzFxuYJFdN9A2XWmKbPSc5gOC1JY5_3uIch_sNijdwNukmN96HjyZfZaDRqVOOcB1wMzEEwfxGrFNqUsfOR4zspYkIEqnOKat93dIviLZ7DNMeHyMI9bC7IuvX0EWgcdzvu5jUzKeSTY6_FZVOLdRK9tHzTHWT6jWvyDJ14tDEUe0BUKxFiMo55czgL8zQBj2eggBH9TTrcwB7dDpMqmIJrj5EXFR7bUAoKyCKikNmkkzgB5ZIGODgBAV6inEfa4caPOyUNOa23hRn_FnYV3_SpxwHGZOkO1oN1SOdv42w6IXG9ce1HrRcb4HCHeBUCdiSazb7vkL0AGM5jWbeb2N-DhyVkklZrlvsKkXRtnGpIY5V-My0003__mC0)
  
  
### 2. Tổ chức các phần tử thiết kế
**Hệ thống được tổ chức theo kiến trúc phân lớp (Layered Architecture), bao gồm các lớp chính:**

**Lớp phần cứng (Hardware Layer):**
- Bao gồm các cảm biến, bộ xử lý chính, nguồn năng lượng và module truyền thông vệ tinh.
  
**Lớp xử lý dữ liệu (Data Processing Layer):**
- Gồm các module xử lý dữ liệu, phát hiện lỗi, và quản lý năng lượng.
  
**Lớp giao tiếp (Communication Layer):**
- Bao gồm các thành phần liên quan đến truyền tải dữ liệu qua vệ tinh.
  
**Lớp lưu trữ (Storage Layer):**
- Quản lý bộ nhớ tạm và dữ liệu lưu trữ dài hạn.

  **Mô hình hóa Kiến trúc phân lớp**
  
  ![Diagram](https://www.planttext.com/plantuml/png/R5BDQiCm3BxxAKJlVO4UHikwiSC2XUm5XArcPh4TP8KGHfziXptINc5uIOgJ-MQaxq-IVxw-Zr6GfNUjwb1_O4EmUyMHc0oSMBzR8Iqzqmu-5S0Tye9i1cI2F-pK1D0jnWWr-HWuArHe_OM3fhYkNy90N8zHoELq56fRA_GOdEkzrIWs-2gOlYK5SCjZd54GPcdhcrAQ12cPFp47FbCQBvTVsi_OjrAXnuOSUIdRhn8MLr6SPIjJI-3qA0YyaUi28uyp9jUUAbao1VFkORz_M0yE1uZaJGJ60GmAAjW04cNhbbWIc29q4uxCGlu7JVnL93Y0CFfu9OuBAxjuCMEN-dStwni5vKjCTiNjBhxEIeHh8a_kDtKaRz97_mK00F__0m00)
  
### 3. Các cơ chế thiết kế được sử dụng
**a. Cơ chế xử lý dữ liệu (Data Processing Mechanism)**
- Dữ liệu từ cảm biến được thu thập, làm sạch và xử lý để đảm bảo tính chính xác.
  
- Xử lý dữ liệu theo chu kỳ, giảm tải cho hệ thống khi năng lượng thấp.

  **Mô hình hóa Cơ chế xử lý dữ liệu**
  
  ![Diagram](https://www.planttext.com/plantuml/png/T94nRiCm301tlOB8L0_vW8OYGzS01Jnq9YH2CM990Kad20g_h4EVr2yKYcKZDX1kedZaKVhx-Js88kiGUtD1TyP0iFj0HVZax4YaIm6Ev4wOEeax-3O0haSHQ2b9vaUYH2IKWQcWRusjj-La0CO5AedQ-8brFM5wa1uLd-76pXxaQxCI609JGALNq1UXdeZR8KRa-qgXrSmOw9ZzqDEY89gh_DHjDRMnSCsThwLCoXrTbrMtWgCnCB_EVl--sTc2KF82Z3Seemni2WgoThIJdS1bdZIHepbGykNd_W400F__0m00)
  
**b. Cơ chế phát hiện lỗi (Error Detection Mechanism)**
- Các thuật toán phân tích dữ liệu được áp dụng để phát hiện bất thường.
  
- Phân biệt lỗi phần cứng (như cảm biến hỏng) và lỗi dữ liệu.

**Mô hình hóa Cơ chế phát hiện lỗi**

![Diagram](https://www.planttext.com/plantuml/png/R951JiCm44NtFiMegsJH2tY1kYZi8Y5wWY7-b0Z74tcSIe1wCXOSYIiWEo4YLRomv3ypx-kFVxw-3veufh7tPk3sZS-WtNsC4kc8X3Pr4gX1-ygXqtv7duQezQnAHqxy6AM5giIYvpDCIYvMZXDREY6en2pKbkO1kFmsHDS5LpmNoqRSwB5GER1__y0_wWfKssdy2OF4jC8-yEXJmu7Fw17I3TSLlzAZLIpJArHj9y3S7g7YBoXIzPBlkLvRUXRnu53C3TriPx-_smveyy8kdOF-RGwESa93smEPj9t9aY8u9PJFcyAekPe3Wik_-mi00F__0m00)

**c. Cơ chế quản lý năng lượng (Power Management Mechanism)**
- Theo dõi mức năng lượng và tự động chuyển đổi chế độ hoạt động (tiết kiệm năng lượng khi pin yếu).
  
- Ưu tiên cung cấp năng lượng cho các thành phần thiết yếu.

  **Mô hình hóa Cơ chế quản lý năng lượng**
  
  ![Diagram](https://www.planttext.com/plantuml/png/Z9112i9034NtFKNeIXTUe0iHroq8wW529zJ1pgHCqXOLJ-R28ta5wLYqBWIpJ5x-_ydZTb-9Oj3MrKc3vH4hWdJ3FGKeq6D5Zhn2GUK1lHMNmYK1A6iKWKXjJwBaOdSenzugXpZAgQDwDiz6K55R6R4mw8MArgXAuJH07LipJgMtMXvsd7CVLmisD46ktma-CGisRKtlBDoeTVPCaTeBLbEHltmI-3foiLZ-iCn0o1k19ZvENgTUanLvCpps2G00__y30000)
  
**d. Cơ chế tự phục hồi (Auto-Reconfiguration Mechanism)**
- Khi lỗi được phát hiện, hệ thống sẽ tự động tái cấu hình để tiếp tục hoạt động.
  
**Ví dụ:**
- Ngắt cảm biến bị lỗi và sử dụng các cảm biến dự phòng nếu có.

**Mô hình hóa Cơ chế tự phục hồi**

![Diagram](https://www.planttext.com/plantuml/png/b591JWCn3Bpd5LPFkuT-80TKKE5M2RKlC8ctHCqcLUnKAgWluy2J-09AThjIqO94RixOCvv9lZu-LooO9FTU7T4SS4-mkCyIbrioCNHkdnEAYm4sP5unEEuNyAu0Z4TcUCBiPOC1zzHJa4sqsLF5ox4aPAJsS9Fe69DeU4mffcqjMZqGZErfKgJTcONwfYlesDHgE4Ld5S1bajzHu9WclPwGSw8r2ZQj7j5INVTnZ2-UcZcg1pI7VFmd8Hfn9vHvncfqNIDmCVo81WFwyzl0R55GmtEAXfZ9bhls9gTAg-2Nj9VBksiGUeoSeIRtvyYDOJrPON0TzEW2y01rw3mhcBTJYEObT9ct35J6O7XyLXUrec3BP_i6003__mC0)
  
**e. Cơ chế truyền thông (Communication Mechanism)**
- Dữ liệu được truyền qua vệ tinh theo lô để tiết kiệm năng lượng.
  
- Hỗ trợ truyền dữ liệu ưu tiên cao (báo cáo lỗi) khi có sự cố khẩn cấp.

  **Mô hình hóa Cơ chế truyền thông**
  
  ![Diagram](https://www.planttext.com/plantuml/png/Z911Qa9138RtSuhWIXTUu2sAKEdkGMbFy3iJxT2PZ4potCWxcGkFv1NAFEI92w5PXV0bNvBRvRfHGxKX9tU4_yM1QV5USXuaUbWiGZtx7qZKlA2p8_89glGDuvIYyJFRW1PM8PgZRM5O1XWw-gp5iog7Lbjrj2ibCUJUKDbpF4tJ866vwkYUEg9njdvWIDP3SE3COdq9G-9P6jZOsyJelwJA4YRyYu-bMhC-WD4vUY5ShzzUFQ2RJrVQjsPgYxZHRLX2U_8V0000__y30000)
  
**f. Cơ chế lưu trữ (Storage Mechanism)**
- Dữ liệu được lưu trữ tạm thời nếu kết nối vệ tinh bị gián đoạn.
  
- Cơ chế nén dữ liệu được áp dụng để tối ưu hóa bộ nhớ.

****Mô hình hóa Cơ chế lưu trữ**

![Diagram](https://www.planttext.com/plantuml/png/j90n2i9044NxESMGoXIvG0f9OHiGz0B3xgZ191jc9e4GSZ8BZ-GLP3LQnDgfFfy7Zp-FsxrG8x6-gQ4ZTwKpOtAm836Kx2xKLjeaE06YgqaLZznqGKZ63pK1lauj2E_8QEF9ACUz1CUgx6ENvZY4oY-ei4d5mvjELoWWpb_R8Yc3x-i_gG1_DsNPTgNEqOHQFR4eHYdCK73huz-U0000__y30000)

### Giải thích biểu đồ:
- Hệ thống trạm thời tiết giao tiếp trực tiếp với hệ thống quản lý dữ liệu **(IDataManagement)** để truyền dữ liệu thời tiết.
- Hệ thống bảo trì sử dụng **IMaintenance** để giám sát, bảo trì, và cập nhật các trạm thời tiết từ xa.
- Hệ thống giao tiếp vệ tinh **(ICommunication)** là trung gian truyền dữ liệu giữa các hệ thống trạm và hệ thống quản lý/lưu trữ.
- Hệ thống dự báo thời tiết sử dụng dữ liệu từ hệ thống quản lý và cung cấp dự báo thời tiết qua **IForecasting.**

## IV.Thiết kế hệ thống con
### 1.1Hệ thống Trạm thời tiết
#### 1.1.1 Hiện thực hóa giao diện 

![PlanText](https://www.planttext.com/plantuml/png/T5JDQXin4BxhAUROGjm7yC649hI5_X2m3pdqecxKbR1MwsfdtVfeSZ2zrQTIGY7k4d8oJMbEAueFQ_8UymHzXIB_iRAt5udLpdpppJUVzDSjZZFa5lD4CnvXQW5EX47BTNUKeKYOCAXm15rXijHcsyzJZlpCff78ijHk3tiY6NGnjJmMsoCuIpyA-veR7ejTt3EUQpmLA7ozNMINez1QeJX9auInJK5eTS9Yq8RdvEOABiZz1At8JN90MTspCAmXxvpS77Jr1uRLDUZgEe6Cobaawr27A05RQCDBHUuo0RGSDBclQeM6rTn8aEIAWJ-TG4JkbWV08Ku3lQVLBDr0FZ9KBdA8gj-F3mdL9TscHNuPKdbZO3abDmQpl3Gnw8SxSeM9MP3JK7lvHP4Rvn19Sf-Dz7kvM45zsuC29FTh_SV4X-I2AOPgzQbS81XoKmL3hn4g8ndN26zMtVPbTMzYt_H_Gc6FTgjJjnoquTN3NGvelUX8vIm1bEI-1rPX4EGqIa6kK045JULCCQ4pqSHXl-L3UowdLG6VDkvZmbomCAVL2IyTjA5dyn6viGbjJkvAUPTDLfrD_JHixjVgHy92Y0PYvzKi0YEfd9ljLbUckyzfNvdUUa3llDVMydp8gImyXpLNfB9GZ9aK1LWLIuJq_G7AYu1-pKo0qjzaAkU3evrQwziL5AYJFdfhl46k5FIbfxBpQgCF-b91GkKDrgVxXB5ZOIxy0_WF003__mC0)

#### -Giải thích về Biểu đồ trình tự:
+ Sensors (Cảm Biến Thời Tiết) gửi dữ liệu thô tới DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ).

+ DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ) thực hiện xử lý và làm sạch dữ liệu.

+ DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ) kiểm tra tính hợp lệ và lỗi của dữ liệu thông qua FaultDetector (Bộ Giám Sát Lỗi).

+ Nếu có vấn đề về năng lượng, DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ) báo cáo và PowerManager (Bộ Quản Lý Năng Lượng) điều chỉnh chế độ năng lượng tự động.

+ DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ) kiểm tra kết nối vệ tinh. Nếu không có kết nối, dữ liệu sẽ được chuyển đến TempStorage (Bộ Lưu Trữ Tạm Thời).

+ Khi kết nối lại, DataProcessor (Bộ Xử Lý Dữ Liệu Tại Chỗ) sẽ gửi dữ liệu đã lưu trữ qua SatelliteComm (Bộ Truyền Thông Vệ Tinh) tới CentralSystem (Hệ Thống Trung Tâm).

+ CentralSystem (Hệ Thống Trung Tâm) xác nhận nhận dữ liệu và SatelliteComm (Bộ Truyền Thông Vệ Tinh) thông báo kết quả truyền tải hoàn tất.



![PlanText](https://www.planttext.com/plantuml/png/X9A_QXj14CRxVOefuy8leC84oqwAn62GYhJBtcHlqTwkcHt9CS55S95QLQeKmgGKCIILbk3YXDzZdo2l4EwFv3lh8Ct13D_lsszcxczyV1rO4iyBAuIoCWIOe0kU0dmM0A2yjQZuJB9yTIHkTvgglYIlC0HFZVAgALjbXLgKxhcKMXDgoTXHvAXcvqIUGjC8wBAfdqX6QmrZssHFDJJ5uigJ96DlkbcgzeGzIOrDaZtGy8HC1XUxpfwxzDT85z99ZUq8HLsSEoHTlL1PNHjM-TGtlObS6ASlV8PTdpToRlaC6HNlTb5uPzZJv2Om5erJLWjgRUZI-s77lYZQ_EYoRdo5Pe5ZxpuQAYGRxxhy61sJjCrJ3TyIpnOBQKtMstntHRT2x4v-VFBYiYDuc-BQG9RYJx0cnQzp8VgI0UP3YckmvP__OFt5ZU2TIV6k02O9DiLlPW3ftMm4f-NAWwe-YxJvuM2xJF4BkEsTqs2V7bAyTth0fR_pqU6CCCiDgF8NpDBcaS6bk1nAq_tpHl3-wM4EJ9KBfysg0CvJ_6vghrbU_dRwqBAVvFZanJc7ecsNvJryQZSi1YmEhb6k5BWyRTRkq4XN_aA8Vm000F__0m00)

#### -Giải thích biểu đồ lớp
+ Sensors -> DataProcessor: Gửi dữ liệu

Sensors(Các cảm biến) gửi dữ liệu thô cho DataProcessor(bộ xử lý dữ liệu).

+ DataProcessor -> DataProcessor: Xử lý dữ liệu

DataProcessor(Bộ xử lý dữ liệu) thực hiện các bước xử lý dữ liệu như làm sạch và tổng hợp dữ liệu.

+ DataProcessor -> FaultDetector: Kiểm tra lỗi

DataProcessor(Bộ xử lý dữ liệu) kiểm tra lỗi và tính hợp lệ của dữ liệu với sự hỗ trợ của FaultDetector(bộ giám sát lỗi) .

+ DataProcessor -> PowerManager: Báo cáo vấn đề năng lượng

DataProcessor(Bộ xử lý dữ liệu)  báo cáo các vấn đề liên quan đến năng lượng cho bộ quản lý năng lượng PowerManager(bộ quản lý năng lượng).

+ DataProcessor -> SatelliteComm: Gửi dữ liệu khi có kết nối

DataProcessor(Bộ xử lý dữ liệu)  gửi dữ liệu đã xử lý tới SatelliteComm(bộ truyền thông vệ tinh) khi có kết nối vệ tinh.

+ DataProcessor -> TempStorage: Lưu trữ tạm thời khi không có kết nối

Nếu không có kết nối vệ tinh, DataProcessor(bộ xử lý dữ liệu) lưu trữ dữ liệu tạm thời trong TempStorage(bộ lưu trữ tạm thời).

+SatelliteComm -> CentralSystem: Gửi dữ liệu đã xử lý

SatelliteComm (Bộ truyền thông vệ tinh) gửi dữ liệu đã xử lý từ các trạm thời tiết tới hệ thống trung tâm CentralSystem(hệ thống trung tâm).

+SatelliteComm -> DataProcessor: Xác nhận dữ liệu đã gửi

SatelliteComm (Bộ truyền thông vệ tinh) gửi thông báo xác nhận việc truyền tải dữ liệu thành công đến bộ xử lý dữ liệu DataProcessor(bộ xử lý dữ liệu).



![PlanText](https://www.planttext.com/plantuml/png/Z9A_IWD14CRxUugFLARm1Ima4D52XSW9sgxdSBUujnVtPls3M5bOfn8H2qqTLBJA8XONV8zv0bz1zh1HKwJOgNP-yyttpLVuwDMi7FlI92hZog7J9yjE6QJdDLFPWQhHJvF4KSRAveRGsIF51Jcah5XN5ga_g7y-NoJ0KagshbpTnVBoAfRM52iCN9LHNLUkYnNi5XvSo7GonA649nWjuTg39RnWDf9mQ_E8-TlOqjQLDumrOefg8srJIxWgmKx1IBZHYt46rIavR2khScenErwcOmlJlCFEhcmEy_aiOMppnNYfOZ96Cw5VbMK4RaYOw5yB7dk54mdNO6sBnR2xL0wHSkLKJX6wzVdimIv2MQOFPVGnt6iS5V4rRpP7rhpYIAOV32jXfDj0_eYBw7uwL-Dir8nn9c7IEi4IxZIALdCXOHJTS3xMvh7yjy6yCNFYtsyUCjYOl_q_Ee-AaiiawP4zZ5Vv3G00__y30000)
#### -Giải thích biểu đồ ngữ cảnh
+ Sensors -> Data Processor: Thu thập dữ liệu tự động

Các cảm biến tự động thu thập dữ liệu từ môi trường (nhiệt độ, độ ẩm, tốc độ gió, v.v.) và gửi dữ liệu này đến Data Processor.

+ Data Processor -> Fault Detector: Kiểm tra lỗi tự động

Data Processor tự động kiểm tra lỗi trong dữ liệu và các cảm biến với sự hỗ trợ của Fault Detector.

+ Data Processor -> Power Manager: Quản lý năng lượng tự động

Data Processor tự động gửi thông tin về trạng thái năng lượng cho Power Manager, giúp hệ thống điều chỉnh sử dụng năng lượng.

+ Data Processor -> Satellite Comm: Gửi dữ liệu qua vệ tinh tự động

Data Processor tự động gửi dữ liệu đã xử lý qua Satellite Comm khi có kết nối vệ tinh.

+ Data Processor -> Temp Storage: Lưu trữ tạm thời khi không có kết nối
  
Nếu không có kết nối vệ tinh, Data Processor sẽ tự động lưu trữ dữ liệu tạm thời trong Temp Storage.

+ Satellite Comm -> Central System: Gửi dữ liệu đã xử lý tới hệ thống trung tâm tự động
  
Satellite Comm tự động gửi dữ liệu đã xử lý từ các trạm thời tiết đến Central System qua vệ tinh.

+ Satellite Comm -> Data Processor: Xác nhận dữ liệu đã gửi
  
Satellite Comm tự động gửi thông báo xác nhận về việc dữ liệu đã được truyền thành công trở lại Data Processor.

### 1.2 Hệ Thống Quản Lý Và Lưu Trữ Dữ Liệu(Data Management and Storage Subsystem)

#### 1.2.1 Hiện thực hóa giao diện 



![PlanText](https://www.planttext.com/plantuml/png/p9F1IiD054NtynMNxls1BgGb0JSMGiSINOxfq0maap3pKjgbAzUkN0aM4K4GTPiWNKJyZ_a2Vq4IgxQbY4ktmpdltVjWtgjbpv8mLAG94n5b1g4K54l3IP3AD8H5o5ak3Ab8vK8JEhuWWO7GOY9JgGb2Zy4fCs8YmOjJExSaqqvZ-WE-vNfIan49sXb3cMTMKMRcBUtvmnsB0fD5qbgb9nXfHPzpWz4ckGgDlXR9t2eB_XCYx6zdI5GgI28mSgoYjkKQxWMSiP1ZRx-DtyM1gnuKngvwHA9STLw0ObTTAP1ovP9OGxLqCEhYs5KFIEeNJEjhpEf5rCBFqRhF_63qBHpMrociAnTHlB6ZyVEuNX3Yva4ZSTMb-b8zVzZ5uTjJ0JADj6w-NjGtcAroC1RsrxgSrFS58bVUDM8nnwnmvIrjXblLQLSSxOQsBk3vmvyLHyQLDvYwwkmFDmlxl0klq9Ccr6t-Yy6yu1_ty88_z-X9FMv-smS0003__mC0)

#### -Giải thích về Biểu đồ trình tự:

+ WeatherStation (WS): Trạm thời tiết gửi dữ liệu thời tiết đã thu thập được đến hệ thống quản lý và lưu trữ dữ liệu.

+ Data Management and Storage Subsystem (DMSS): Hệ thống nhận dữ liệu thời tiết và chuyển tiếp đến bộ xử lý dữ liệu.

+ Data Processing Unit (DPU): Xử lý dữ liệu thô, làm sạch dữ liệu, phát hiện lỗi, và xác thực dữ liệu trước khi lưu trữ.

+ 

+ Data Interface ( Giao Diện Dữ Liệu) nhận dữ liệu từ Repository(Kho Dữ Liệu Trung Tâm) và cung cấp cho Central System ( Hệ Thống Trung Tâm) khi có yêu cầu truy xuất.



![PlanText](https://www.planttext.com/plantuml/png/d9I_Qi907CVtUueVJksW3-1GXBeKB9J6KjVhUKq2oILSVW53wT2fQ_C65N4KxPf3EaHyZtk2la99r6fCOxN3BGVVFx_F_RWlzTaAa4eCNOSmXmO1rEuvHOjBC92YxOaQF140CBMQs6sjfXrRgzVmx9myautYaWkKr04Z2f2xQm7ACEg5EXbZXQfDaS8r5TJaBXS8LFJ1G4zIauCHFWIxPivo5dQbLjE25m0Cj9fqqddfEXsohgNL1_kZSbxYbljUOACdevsuhN3nbevwgvoL-t6ZtKYFyI2mXGbtmiQrTKLX9trt3PqCcNNoA7dObK0k7odZX-bdIJePH_jMvKUlro-gvcYkbW7wMat1oLq0hUpePEB38bxEj1enKY7FdIlvDtFuWDbZ5n8MSJhAwO6JpacrmRRu3fCci52Om7GozikksqHIKXRQRXQycVE5GGvuru-GOzUwqJZ0Tn7RMhs4u5jQnVRFr8Maau8EuDxB-ft-FyOgqDyBgQJNugAVVKNV0000__y30000)

#### -Giải thích biểu đồ lớp
+ Weather Station:

gửiDữLiệu(): Gửi dữ liệu thu thập được từ các cảm biến vào Data Processing Unit.

+ Weather Station:

gửiDữLiệu(): Gửi dữ liệu thu thập được từ các cảm biến vào Data Processing Unit.

+ Data Management and Storage Subsystem:

lưuTrữDữLiệu(): Lưu trữ dữ liệu vào Central Data Repository.

xửLýDữLiệu(): Xử lý và làm sạch dữ liệu.

xácThựcDữLiệu(): Xác thực dữ liệu trước khi lưu trữ.

+ Central Data Repository:

lưuDữLiệuĐãXửLý(): Lưu trữ dữ liệu đã xử lý.

truyXuấtDữLiệu(): Cung cấp dữ liệu đã lưu trữ khi có yêu cầu.

+ Data Processing Unit:

xửLýDữLiệu(): Xử lý và tổng hợp dữ liệu từ các cảm biến.

làmSạchDữLiệu(): Làm sạch dữ liệu thu thập được.

xácThựcDữLiệu(): Xác thực dữ liệu trước khi lưu trữ.

+ Data Interface:

truyXuấtDữLiệu(): Truy xuất dữ liệu từ Central Data Repository.

lấyDữLiệu(): Lấy dữ liệu từ Central Data Repository khi có yêu cầu.


![PlanText](https://www.planttext.com/plantuml/png/Z94nQiD044NxFSN7lI-W8ZZOa1HA4MIIUY8jac2rCgjPI0YfNUi60P5InBKMaqB6zzWJv0fXJHhRZOgPOc3--_Fdr_qi6YR3jbA2KguDdYLn8Kt2n6Mj_uTOIis6LFBMiAo4C39bqhcIcDrxjyMwyAxLEHwj7pgDUDpZQVn4VDnPh8rttrY55fVURUqCr615J0-aAPULr7ohiuHhGxbCx4jpWk1TuC8CvlER2OiHxhphIsG1gKv8S17A3_q6X_QuywvB1IPe1UA5YIXSD7HdyeTsxF3gNGyrxYSBduMA24khSwH--DfSYwiG9OSenOSG2wcpyB8_0000__y30000)

#### -Giải thích biểu đồ ngữ cảnh

+ Weather Station(Trạm thời tiết) gửi dữ liệu thu thập được từ các cảm biến tới Data Processing Unit.

+ Data Processing Unit xử lý dữ liệu và sau đó gửi dữ liệu đã xử lý đến Central Data Repository để lưu trữ.

+ Central System(Hệ Thống Trung Tâm) có thể truy xuất dữ liệu từ Data Interface.

+ Data Interface lấy dữ liệu từ Central Data Repository để cung cấp cho Central System(Hệ Thống Trung Tâm) khi có yêu cầu.
  
### 1.3 Hệ Thống Bảo Trì Và Cấu Hình Từ Xa
#### 1.3.1 Hiện thực hóa giao diện 


[![PlanText](https://www.planttext.com/plantuml/png/h9GzRi9048Lxd-A9FXUWY90eKaIfA99sSLRiIdYCx7516QMWpWrYHGW9XGli5Yds97E2N242J6A3WF3JJ34_txnvMkst_-hah38kac6aOaupj1wK9TQaADReZNFMIGigHoszpcxw7xLYepFqMB5D2RsYd_-DLTMg-5lR37SrSQQ6zKLLgbeIxUp5pUq-Ajgu4x-m68TvWLZSR1KN8v0Hjs2CZBWP8H7_aaJx80VvzrRyQmBE54R6XZcXB-w3ha3kdYDqrvqsda8PhpdKlDwauPt0ugPy5L-d1Kpu98EXkD9Ux6UTQApuoKhhkU3kjZuOyHEm4Vz6WmiztIRNZMsyNvncwi26Ca4UIWQl-9o9Am_BFORlXp95l0mDvB_jQDvpX1f57KtFoz_a1m00__y30000)

#### -Giải thích về Biểu đồ tuần tự:

+ Maintenance System: Hệ thống bảo trì gửi yêu cầu cập nhật phần mềm và cấu hình lại cho trạm thời tiết.

+ Weather Station Subsystem: Hệ thống con của trạm thời tiết thực hiện các hành động bảo trì và cấu hình từ xa.

+ Central System: Hệ thống trung tâm yêu cầu báo cáo tình trạng từ trạm thời tiết.




[![PlanText](https://www.planttext.com/plantuml/png/V98nJiCm58Ptd-AfKplq0WoeQWSwK5GfaH2Z6wpO8dcfaXUa2XWG0pCtm48eKaKka0mCFebFm1MGaqPgeEtoBtv-__V_za_zFSc8fvJ74GiYdcKmM725991Z8C3RP2JY0Jmm00XjNQeRiyrdjYgSbEihQQkIbj9M1Ivi_HmFHmSdF_Ev-K9vQIkjTYFAwDWpcdntuAUsqXZERVtgIrk_OJWSiIVM8LqBJbAau14dbI1u-IhR9xjJjdw9_PGlfJ9RdDhg0_z11IU0WpvYdwCBD3KwcHcTx1FtC6S2AULHlxLDLyEHwm203WgFhp_u9EFnu_d9PixWmb4t02vWqMYvRkq8raq94BiMuDwyjoM0TFOGkHhOgVMj_z_8dUdAw0G29zJiepOFOnE1j-wp_G800F__0m00)

#### -Giải thích biểu đồ lớp
+ Maintenance System: Là lớp đại diện cho hệ thống bảo trì. Các phương thức của lớp này gồm:
  
gửiYêuCầuCậpNhậtPhầnMềm: Gửi yêu cầu cập nhật phần mềm.

gửiYêuCầuCấuHìnhLại: Gửi yêu cầu cấu hình lại hệ thống.

giámSátTìnhTrạngHệThống: Giám sát và theo dõi tình trạng hệ thống.



+ Weather Station Subsystem: Là lớp đại diện cho hệ thống con của trạm thời tiết. Các phương thức của lớp này gồm:

kiểmTraPhiênBảnPhầnMềm: Kiểm tra phiên bản phần mềm hiện tại của trạm.

cậpNhậtPhầnMềm: Cập nhật phần mềm của trạm.

cấuHìnhLạiHệThống: Cấu hình lại hệ thống khi có yêu cầu.

gửiBáoCáoTìnhTrạng: Gửi báo cáo tình trạng hệ thống.



+ Central System: Là lớp đại diện cho hệ thống trung tâm. Các phương thức của lớp này gồm:
  
yêuCầuBáoCáoTìnhTrạng: Yêu cầu báo cáo tình trạng từ trạm thời tiết.

nhậnBáoCáoTìnhTrạng: Nhận báo cáo tình trạng từ trạm thời tiết.




[![PlanText](https://www.planttext.com/plantuml/png/b98zJiGm48Lxd-8fDNi12hGe1HKDAH2bDp5nf6IoSiP8255GKNC3Kg2L4Bc0Kr3a93u1Lq3vMKYWIkFYwPltvcdyrNvkAvQ6RP4B6NDf45mhoLePH2mvAoc0h31fatGaGqLiP8xelc9L3E0aZSgHkvGPiI99iPgpCtdYXL4nIqfpXU1A5IMhEGH92SAIRhFKcc4HH7PN_HgE8xE9SqeM_0-E1u4_fR3PdArnECM5RviCt7sG1XllQagXVViCrhvzeLJWVyNrAQ5tpHwalMiOU-tTWL3uzgauGUpTcuKU5iYzgpE1vG7MfzrqxxRtFLZSTQzZB67NrINY_bcq5Oz2R1Kb_UVv1W00__y30000)


#### -Giải thích biểu đồ ngữ cảnh
+ Weather Station: Gửi tình trạng hệ thống.

+ Central System: Yêu cầu và nhận báo cáo tình trạng của hệ thống.

+ Maintenance System: Cập nhật phần mềm và cấu hình lại hệ thống.


### 1.1 Hệ Thống Truyền Thông
#### 1.1.1 Hiện thực hóa giao diện 

[![PlanText](https://www.planttext.com/plantuml/png/Z9EnIWD148RxVOh_1No1524GmIBQ647RzRBabknDucKkO2aMgLDO2Waf9MXXTOkaEF4zvWby1LcqkBsSa6vXThwP__ztl_s-DsUTSv4vDTCvsyJED36kZURKv4FMRASKbJ3KR9opRFhJB8jAfvhrXIOzDfaXZafzGvnh5svScjbKgNW2JhgDcUZWAYt0gPIx6KRYN-6i-6K15l-2HCfjXbihvPwEOTs8ty5L7rXKwq1ueZ5IyTi8tGAAnAA3C_4x6wtpkQgs4L75FIsGWHN_c85pZOcKUmQ9Nrain2_1bbAb7MDGgt1QhIb5KhtJM06D3CA8sFfWNbxSYt-WQDUxGjUc152ZxwJRJ0eTd7-z5U0ySEfcjRSVEbzj4b28aNwz-ZlNKSRDJIHuaWQfXxgFIBfzMx2Kcomy9_zi_q4rO-g7or52JigDLOP6IlKCZSAl-G400F__0m00)

#### -Giải thích biểu đồ trình tự

+ Trạm Thời Tiết (Weather Station): Đại diện cho các trạm thời tiết, nơi thu thập và xử lý dữ liệu từ các cảm biến.

+ Bộ Truyền Thông Vệ Tinh (Satellite Communication Module): Chịu trách nhiệm kiểm tra kết nối vệ tinh và truyền dữ liệu từ trạm thời tiết về trung tâm.

+ Hệ Thống Quản Lý Dữ Liệu (Data Management System): Nhận và xử lý dữ liệu từ trạm thời tiết và gửi đến kho dữ liệu trung tâm.

+ Kho Dữ Liệu Trung Tâm (Central Data Repository): Lưu trữ dữ liệu từ các trạm thời tiết.


[![PlanText](https://www.planttext.com/plantuml/png/X991QWCn34NtSmgHLRl81MPH0ickIHSTGxiLCo8sjULWIv0Xv6HTz4YzGidKquQcaomjvFVu7ts-VoooO18DlcezvWop5qAnbA0H51Tv1eSA0CIgiRXRwTgHtjsVHdjTz-TlhsgI6Wp6HlSzsghxsJXMew518U-T42nZ2Cgk7KomYPrwAi8tHy4aV2Hv6ccIj2U-flnrh50GDiYufK0iqFHPA1GsM-HhIVRO6gljfUcVC4jYIUXX43xJBcOdCVN5zETR2V6gAEUeoyxdyuVRFTMGYRiC7GfMDxS7v5GjDKX2pi79Y9lQ732JeMl84XCLo8AuErtM5m000F__0m00)


#### -Giải thích biểu đồ lớp

+ Weather Station gửi dữ liệu tới Satellite Communication Module.

+ Satellite Communication Module truyền dữ liệu tới Data Management System.
  
+ Data Management System lưu trữ dữ liệu vào Central Data Repository.





[![PlanText](https://www.planttext.com/plantuml/png/V94nJiD044NxFSLNggJ81L95meA6q1XmFN96oKhhTRGxHbY8Ye93qD1GMb1xXL94uXvx0gw0xCWeYWZrU_FdQ-OxRETUo4bL64Mvb0wZZ4dMx90AYIxj2EIHfGDDITWOBOopiYWgg_FUGbfxuQANKvB1JaW82xAqueAj75h9uZVpnhFp60-Bpql7ENbXvoUzsdEb7ET2TcKOexztFoWWIp6TOdmHGwEHnF2EInt3SpLHw8gTXibYFtcrZcrZZ-c-OiUlNLNZDhPlHywZKgVpCKE-hkeOdYn4ntQxmRB3fiUG65vqVv5_Mc26-nWQcDqdxdQlC5yV5SHrna6MchDTTj_y0G00__y30000)

#### -Giải thích biểu đồ ngữ cảnh

+ Weather Station (Trạm Thời Tiết): Gửi dữ liệu thu thập được từ các cảm biến thời tiết.

+ Satellite Communication System (Hệ Thống Truyền Thông Vệ Tinh): Chịu trách nhiệm truyền tải dữ liệu từ Trạm Thời Tiết tới Hệ Thống Quản Lý Dữ Liệu.

+ Data Management System (Hệ Thống Quản Lý Dữ Liệu): Nhận và xử lý dữ liệu từ hệ thống truyền thông vệ tinh, sau đó lưu trữ và quản lý chúng.

+ Users (Người Dùng - Dự Báo Thời Tiết): Truy vấn và yêu cầu dữ liệu từ Hệ Thống Quản Lý Dữ Liệu để phục vụ cho công tác dự báo thời tiết hoặc phân tích khí hậu.

+ Communication System: Hệ thống truyền thông bao gồm các chức năng gửi và nhận dữ liệu qua vệ tinh giữa các thành phần trong hệ thống.

- Các mối quan hệ:

+ Weather Station gửi dữ liệu tới Satellite Communication System để truyền tải dữ liệu.

+ Satellite Communication System chuyển tiếp dữ liệu tới Data Management System.

+ Users có thể truy vấn dữ liệu từ Data Management System để phục vụ cho các mục đích dự báo hoặc phân tích thời tiết.

  # V.Thiết kế lớp
# 1.1 Sensors(Cảm biến)
- Định nghĩa: Lớp này đại diện cho các cảm biến được sử dụng để đo các yếu tố khí tượng như nhiệt độ, độ ẩm, áp suất, gió.

## Thuộc tính:
- sensorID (string): Mã ID của cảm biến.
- sensorType (string): Loại cảm biến (nhiệt độ, độ ẩm, gió, v.v.)
- value (float): Giá trị đo được từ cảm biến.
- status (string): Trạng thái của cảm biến (hoạt động, hỏng hóc)
## Phương thức:
- collectData(): Thu thập dữ liệu từ cảm biến.
- checkStatus(): Kiểm tra trạng thái của cảm biến.
- reset(): Đặt lại cảm biến về trạng thái ban đầu.
## Lý do cần có:
- Cảm biến là thành phần chính thu thập dữ liệu khí tượng từ môi trường. Chúng cần có các phương thức để đọc và hiệu chỉnh dữ liệu, đảm bảo dữ liệu chính xác cho các bước tiếp theo của hệ thống.
## Hình ảnh mô tả lớp Sensors(Cảm biến):

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK9mQbvnVb6nGZMN0WWKWxcUBbOAnIL5cNdfoA8XbGMfgE9bYJcbgLOAQJdvYILGbIM99QN5gAgIytDoKfDBN19B4ZKqhHJAyZDJe18PgSdPmM0Tg195gSMf9N2XMYuk00000F__0m00)
# 1.2 DataProcessor (Xử lý Dữ liệu)
- Định nghĩa: Lớp này xử lý dữ liệu từ các cảm biến để tính toán các giá trị khí tượng như nhiệt độ trung bình, độ ẩm, v.v.

## Thuộc tính:
- rawData (list): Dữ liệu thô từ cảm biến.
- processedData (dict): Dữ liệu đã xử lý.
- processingTime (float): Thời gian xử lý dữ liệu.
## Phương thức:
- processData(): Xử lý dữ liệu thô từ các cảm biến để tính toán các giá trị khí tượng.
- validateData(): Kiểm tra tính hợp lệ của dữ liệu (loại bỏ dữ liệu nhiễu).
- formatData(): Định dạng dữ liệu cho phù hợp với hệ thống lưu trữ.
## Lý do cần có: 
- Lớp này thực hiện các thao tác xử lý dữ liệu thô để chuyển thành thông tin hữu ích cho các hệ thống khác. Các phép toán xử lý như tính trung bình, lọc nhiễu, hoặc phân tích là rất quan trọng để đảm bảo dữ liệu chính xác và có ý nghĩa.
## Hình ảnh mô tả lớp DataProcessor (Xử lý Dữ liệu):

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9BOabYG55-ScfnSNwHGZMN0WWK9PQ3nAqKSZABIo121H0rgIaGYPJCP5I9pBpqaCpSL2k5j9pyH5Gfa0uDJIk5ilpC58X4MM9EPafYIIgcJ5f-KMvY2OfuBHSN0000__y30000)



# 1.3 FaultDetector (Phát hiện Lỗi)
- Định nghĩa: Lớp này phát hiện các lỗi trong các cảm biến hoặc trong dữ liệu thu thập được.

## Thuộc tính:

- errorLog (list): Nhật ký lỗi đã phát hiện.
- threshold (float): Ngưỡng lỗi cho phép.
- sensorStatus (string): Trạng thái cảm biến (hoạt động, lỗi).
## Phương thức:

- detectFault(): Phát hiện lỗi trong dữ liệu hoặc cảm biến.
- logError(): Ghi lại lỗi vào nhật ký.
- resetFault(): Đặt lại trạng thái lỗi sau khi khắc phục.
## Lý do cần có: 
- Trong môi trường hoang dã, các cảm biến có thể gặp sự cố. Lớp này giúp đảm bảo rằng các lỗi trong dữ liệu sẽ được phát hiện và xử lý kịp thời, tránh gây ảnh hưởng đến các phân tích và dự báo sau này.
## Hình ảnh mô tả lớp FaultDetector (Phát hiện Lỗi):

![Diagram](https://www.planttext.com/plantuml/png/N8mn3i8m40Hxl-9A-88h2a95nmki-70i7Jdfzao3U1a5J-8BA35Ds79cDP_N-m1FvkqcOPG4q2aryICxZwv6Zq3Bs4pjh2MIL7XdFXbZKicHhgBfHy4pr2wUl24ItEfSkibhSytlzf7kMdCNecLO-bjg3FvxFqFu0W00__y30000)
# 1.4 PowerManager (Quản lý Nguồn)
- Định nghĩa: Lớp này quản lý nguồn năng lượng của trạm khí tượng, bao gồm việc giám sát mức pin và tiết kiệm năng lượng.

## Thuộc tính:

- batteryLevel (float): Mức năng lượng của pin (từ 0 đến 100).
- powerStatus (string): Trạng thái nguồn (on/off).
- powerUsage (float): Mức tiêu thụ năng lượng.
## Phương thức:

- monitorPower(): Giám sát mức năng lượng của hệ thống.
- switchToLowPowerMode(): Chuyển sang chế độ tiết kiệm năng lượng khi pin yếu.
- chargeBattery(): Sạc lại pin khi cần thiết.
## Lý do cần có: 
- Trạm khí tượng hoạt động trong môi trường hoang dã, có thể không có nguồn điện liên tục. Quản lý năng lượng là rất quan trọng để đảm bảo hệ thống vẫn hoạt động hiệu quả mà không gặp phải tình trạng hết pin.
## Hình ảnh mô tả lớp PowerManager (Quản lý Nguồn)

![Diagram](https://www.planttext.com/plantuml/png/L8v12i8m44NtFSKizGfPYUiAWdg0CHtJG9gHcMc3Y2TpuP6yWjI0sBzz3_vxFryRDHGRXzJuXAgmvqAomuo11EuDp3kZ6ScjfOcIWqjYj0gkitmmj54Tg4dCuG-S50Cj_85pD9RlnshjOEBOLQ8bck-Ft7Af1TpHql0zIg1jJVcXH_C1003__mC0)
# 1.5 TempStorage (Lưu trữ Tạm thời)
- Định nghĩa: Lớp này lưu trữ dữ liệu tạm thời trong quá trình xử lý trước khi đưa vào hệ thống lưu trữ chính.

## Thuộc tính:

- tempData (dict): Dữ liệu tạm thời.
- storageCapacity (float): Dung lượng lưu trữ tạm thời.
- usedStorage (float): Dung lượng đã sử dụng.
## Phương thức:

- storeData(): Lưu trữ dữ liệu tạm thời.
- retrieveData(): Lấy dữ liệu đã lưu trữ tạm thời.
- clearStorage(): Xóa dữ liệu tạm thời khi không cần thiết.
## Lý do cần có: 
- Dữ liệu thu thập từ cảm biến cần được lưu trữ tạm thời trước khi xử lý hoặc lưu trữ lâu dài. Lớp này giúp tối ưu hóa hiệu suất hệ thống bằng cách giảm tải cho bộ nhớ chính.
## Hình ảnh mô tả lớp TempStorage (Lưu trữ Tạm thời)

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK98Qcv1S4b-KM9wga8rbm88bAJc5hWabYHQAQHa9fT0n8eXIfmJ2nAJCqighHJISl8JeNAbnQafK2DGn45wKa46QMXQAPJbPwP0X8jIIueoKykmo2Jdf2OMGKs2ozHo0G000F__0m00)
# 1.6 SatelliteComm (Giao tiếp Vệ tinh)
- Định nghĩa: Lớp này cung cấp các phương thức để giao tiếp với vệ tinh, gửi và nhận dữ liệu.

## Thuộc tính:

- satelliteConnection (bool): Kết nối với vệ tinh (True/False).
- signalStrength (float): Cường độ tín hiệu từ vệ tinh.
- satelliteID (string): Mã ID của vệ tinh.
## Phương thức:

- sendData(): Gửi dữ liệu lên vệ tinh.
- receiveData(): Nhận dữ liệu từ vệ tinh.
- checkConnection(): Kiểm tra kết nối với vệ tinh.
## Lý do cần có: 
- Trong môi trường hoang dã, việc truyền tải dữ liệu qua các kênh truyền thông vệ tinh là thiết yếu để gửi dữ liệu về trung tâm quản lý. Lớp này đảm bảo quá trình truyền thông luôn ổn định.
## Hình ảnh mô tả lớp SatelliteComm (Giao tiếp Vệ tinh)

![Diagram](https://www.planttext.com/plantuml/png/PCqn3i8m30NGFQVm25V8X4GNvfx0f2QrS6mfCLqG9sFWI5oXggYe17_yJr___NmTccFrMv6G15k37fr4sEbefS0zm9AsbQgKd4qZdCraPSwAqdibpJv6k8YX_onFNOJcbJMlG3fqwBZRHvYCXqzRAH5Fz0zff7JTth_u23C0003__mC0)
# 1.7 CentralSystem (Hệ thống Trung tâm)
- Định nghĩa: Lớp này là trung tâm điều phối toàn bộ hoạt động của trạm khí tượng, bao gồm việc giám sát các cảm biến, xử lý dữ liệu và cảnh báo.

## Thuộc tính:

- status (string): Trạng thái của hệ thống trung tâm (hoạt động, bảo trì).
- sensorList (list): Danh sách các cảm biến kết nối với hệ thống.
- dataLog (list): Nhật ký dữ liệu.
## Phương thức:

- monitorSystem(): Giám sát trạng thái hoạt động của toàn hệ thống.
- processData(): Xử lý dữ liệu từ các cảm biến.
- sendAlert(): Gửi cảnh báo khi có sự cố.
## Lý do cần có: 
- Hệ thống trung tâm là bộ điều khiển chính của trạm khí tượng, giúp điều phối các hoạt động của các hệ thống con và đảm bảo sự hoạt động liên tục của trạm.
## Hình ảnh mô tả lớp CentralSystem (Hệ thống Trung tâm)

![Diagram](https://www.planttext.com/plantuml/png/LCmn2W8n58JXFgT8gLT8fMYvdITuR1vB89idRsO54KzciKVo2Y8HqIc_7-RvM7UWE9UvXh4A40_Qw59FLr3dU0lnFL2u84NGIvi-fWtcGm5Jh0NiceKosFHBixL2y_wusQPuiP9xEhkD2Xo5yX-WBU-hEhzy3oy0003__mC0)
# 1.8 WeatherStation (Trạm Khí tượng)
- Định nghĩa: Lớp này đại diện cho một trạm khí tượng, chịu trách nhiệm thu thập và gửi dữ liệu khí tượng.

## Thuộc tính:

- location (string): Vị trí của trạm khí tượng.
- weatherData (dict): Dữ liệu khí tượng thu thập được.
- systemStatus (string): Trạng thái của hệ thống (hoạt động, bảo trì).
## Phương thức:

- initialize(): Khởi tạo trạm khí tượng.
- collectWeatherData(): Thu thập dữ liệu khí tượng từ các cảm biến.
- sendWeatherData(): Gửi dữ liệu khí tượng tới hệ thống trung tâm.
## Lý do cần có: 
- Trạm khí tượng là trung tâm của toàn bộ hệ thống, nơi các cảm biến và thiết bị được đặt để thu thập dữ liệu khí tượng.
## Hình ảnh mô tả lớp WeatherStation (Trạm Khí tượng)

![Diagram](https://www.planttext.com/plantuml/png/R8sn3K8n34JxJE4ILaX5mGOKr5PYWIN_H8hlWm0n6SKVYHLG2CsNS7VlpdVlrx9pSCCyMKZ6xdGKnbdQ0GojXHw1-bbDNnt9qRIS1hsEx9x1aR8c3EmtXqozOVRrWnQ5ikbTDjj8bwfvy5JD9E6ttVlMlal9_ynd-0000F__0m00)
# 1.9 Data Management and Storage Subsystem (Hệ thống Quản lý và Lưu trữ Dữ liệu)
- Định nghĩa: Lớp này quản lý việc lưu trữ và truy xuất dữ liệu từ hệ thống trạm khí tượng.

## Thuộc tính:

- storageCapacity (float): Dung lượng lưu trữ của hệ thống.
- dataRepository (dict): Kho dữ liệu chứa các bản ghi khí tượng.
- accessLog (list): Nhật ký truy cập dữ liệu.
## Phương thức:

- storeData(): Lưu trữ dữ liệu vào kho.
- retrieveData(): Truy xuất dữ liệu từ kho.
- deleteData(): Xóa dữ liệu khi không cần thiết.
## Lý do cần có: 
- Dữ liệu khí tượng cần được lưu trữ một cách an toàn và có thể phục hồi khi có sự cố. Lớp này giúp quản lý và bảo vệ dữ liệu dài hạn.
## Hình ảnh mô tả lớp Data Management and Storage Subsystem (Hệ thống Quản lý và Lưu trữ Dữ liệu)

![Diagram](https://www.planttext.com/plantuml/png/R8qn2W8n44NxFSMKUeLKWfRQw0a-oHW2oSwI6HU2xCaiF99NaB3R2FxoFNZ_yteVr53jKVBWCrJf1CC58o8N7ktMrBZGSw0-DQc8VCG4dwmvkcU1hIx0SEL9D9dKvYWalnbupwfdYOvoqWts5FUltTxHB2cikBBLnFCV4pYp_V9b-0800F__0m00)
# 1.10 DataProcessingUnit (Đơn vị Xử lý Dữ liệu)
- Định nghĩa: Lớp này chịu trách nhiệm xử lý dữ liệu khí tượng thu thập từ các cảm biến, bao gồm việc phân tích và tính toán các chỉ số khí tượng.

## Thuộc tính:

- processorSpeed (float): Tốc độ xử lý dữ liệu.
- dataQueue (list): Hàng đợi dữ liệu cần xử lý.
- processingTime (float): Thời gian xử lý dữ liệu.
## Phương thức:

- processData(): Xử lý dữ liệu nhận được từ các cảm biến.
- queueData(): Đưa dữ liệu vào hàng đợi xử lý.
- clearQueue(): Xóa hàng đợi khi xử lý xong.
## Lý do cần có: 
- Đơn vị này giúp thực hiện các phép toán xử lý phức tạp như phân tích, dự báo và báo cáo kết quả khí tượng.
## Hình ảnh mô tả lớp DataProcessingUnit (Đơn vị Xử lý Dữ liệu)

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9BOabYG55-ScfnSMPUUcXUPeb2DPS221H0HFEBWWjIKrEi5D9oyXDB858fYIM9WQMffQbM2ZcPnL11gFhClFIGpDnK5FLGAP1T6ffM2cNvcIaGYKAG8PZ2oJcfYKLW2-3YjLm00000__y30000)
# 1.11 DataInterface (Giao diện Dữ liệu)
- Định nghĩa: Lớp này cung cấp giao diện giữa người dùng và hệ thống, cho phép người dùng truy cập và xem dữ liệu khí tượng.

## Thuộc tính:

- interfaceType (string): Loại giao diện (giao diện người dùng, API).
- connectionStatus (bool): Trạng thái kết nối.
- userPermissions (string): Quyền truy cập của người dùng.
## Phương thức:

- displayData(): Hiển thị dữ liệu cho người dùng.
- connectToSystem(): Kết nối với hệ thống.
- sendData(): Gửi dữ liệu cho hệ thống khác.
## Lý do cần có: 
- Giao diện dữ liệu giúp người dùng hoặc các hệ thống khác có thể dễ dàng truy cập và tương tác với dữ liệu khí tượng.
## Hình ảnh mô tả lớp DataInterface (Giao diện Dữ liệu)

![Diagram](https://www.planttext.com/plantuml/png/L8qn2W8n44Nxd2AbNY6LXOsTi7k1CHbb89bPCXCXo9xCmYDv1LaMY_poFzx_t_Vdf0RLMiakPb3rPp2ui66zGqJ_SduB_OkvBnYyMYL-x2WACqOZuSd0cWP_4yaxQuhrYhMGAWdhA2RI9KFV_Wx7u9z2QLYSPUfgM4Qeo6bGLlS3003__mC0)
# 1.12 MaintenanceSystem (Hệ thống Bảo trì)
- Định nghĩa: Lớp này giúp giám sát và quản lý các công việc bảo trì của hệ thống trạm khí tượng.

## Thuộc tính:

- maintenanceLog (list): Nhật ký bảo trì.
- maintenanceStatus (string): Trạng thái bảo trì (cần bảo trì, không cần bảo trì).
- schedule (string): Lịch trình bảo trì.
## Phương thức:

- performMaintenance(): Thực hiện công việc bảo trì cho hệ thống.
- logMaintenance(): Ghi lại thông tin bảo trì vào nhật ký.
- scheduleMaintenance(): Lên lịch bảo trì cho hệ thống.
## Lý do cần có: 
- Hệ thống bảo trì giúp đảm bảo rằng các thiết bị trong trạm khí tượng luôn hoạt động tốt, giảm thiểu thời gian gián đoạn.
## Hình ảnh mô tả lớp MaintenanceSystem (Hệ thống Bảo trì)

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9lOcPUIMfUObvoQd1bSKbgha8rbm88v28aVFBJhHHoCejBC6I2In9BIekj58fBYZBpqY7InSaPgIcbEQceeWMfHMdvHRb8rcbeMYcKvMUcGEHpyjDnoi5CnAQWbWi0003__mC0)
# 1.13 WeatherStationSubsystem (Hệ thống Con Trạm Khí tượng)
- Định nghĩa: Lớp này đại diện cho các hệ thống con của trạm khí tượng, mỗi hệ thống con có thể bao gồm một số cảm biến hoặc thiết bị phụ trợ.

## Thuộc tính:

- sensorList (list): Danh sách cảm biến trong hệ thống con.
- status (string): Trạng thái của hệ thống con.
- location (string): Vị trí của hệ thống con.
## Phương thức:

- initialize(): Khởi tạo hệ thống con.
- collectData(): Thu thập dữ liệu từ cảm biến.
- sendData(): Gửi dữ liệu lên hệ thống trung tâm.
## Lý do cần có: 
- Hệ thống con giúp chia nhỏ và quản lý các thành phần trong trạm khí tượng.
## Hình ảnh mô tả lớp WeatherStationSubsystem (Hệ thống Con Trạm Khí tượng)

![Diagram](https://www.planttext.com/plantuml/png/LCmn3i8m44JHFgTm2LTmHK59bu9wSLQmqiQMF6CaG9mi1KVY2WX2uodVIF-zl7QWLBRPX-G2XACABrf72gtaiPrm0tKEZo5y1yqezM1W36xWNobiY06ibi-hUKc_HA-MZIPkTzriOxWMcrPFnLqJzqBf3sYUEdqE7m000F__0m00)
# 1.14 SatelliteCommunicationModule (Mô-đun Giao tiếp Vệ tinh)
- Định nghĩa: Lớp này quản lý giao tiếp giữa trạm khí tượng và vệ tinh.

## Thuộc tính:

- satelliteID (string): Mã ID của vệ tinh.
- signalStrength (float): Cường độ tín hiệu.
- communicationStatus (string): Trạng thái giao tiếp.
## Phương thức:

- connect(): Kết nối với vệ tinh.
- sendData(): Gửi dữ liệu lên vệ tinh.
- receiveData(): Nhận dữ liệu từ vệ tinh.
## Lý do cần có: 
- Mô-đun giao tiếp vệ tinh rất quan trọng để đảm bảo rằng trạm khí tượng có thể truyền tải dữ liệu trong những khu vực không có mạng thông thường.
## Hình ảnh mô tả lớp SatelliteCommunicationModule (Mô-đun Giao tiếp Vệ tinh)

![Diagram](https://www.planttext.com/plantuml/png/L8mn3i8m40Hxly8bV24L4caegFA2atsOaovtahrEWtWP1K_Y2mWH9BBbpkwy7iz30rNqMKDIQYrE15OLyD7dkPiaWhYTFNVbU0lna_RRdCOXDbIniW8fHZgXiXLSXtXH9tnH-jTD8FIs_IOtuuJTVeYBIrw5R7aaqBQjd5WMte1xU0C00F__0m00)
# 1.15 CentralDataRepository (Kho Dữ liệu Trung tâm)
- Định nghĩa: Lớp này chứa tất cả dữ liệu khí tượng đã được thu thập và xử lý.

## Thuộc tính:

- repositorySize (float): Dung lượng kho dữ liệu.
- dataRecords (list): Danh sách bản ghi dữ liệu.
- accessHistory (list): Lịch sử truy cập dữ liệu.
## Phương thức:

- storeData(): Lưu trữ dữ liệu vào kho.
- retrieveData(): Truy xuất dữ liệu từ kho.
- archiveData(): Lưu trữ dữ liệu lâu dài.
## Lý do cần có: 
- Người dùng cần có quyền truy cập vào dữ liệu và cấu hình của hệ thống khí tượng.
## Hình ảnh mô tả lớp CentralDataRepository (Kho Dữ liệu Trung tâm)

![Diagram](https://www.planttext.com/plantuml/png/R8qz2e9130NxFKLAlS9MWXRMUeAGZHY8HfBuWOedi_18Na7MFqHyvGp3krskaqZqt6-qa684J7cRZZh3n0NlB2JD3t0gqESVifGZLrYfOJvLUmHatgA2Ihmm4d74NA97tw83xY-ZSON1fBqVqeM7FmQTrl8ZpkKE003__mC0)
# 1.16 CommunicationSystem (Hệ thống Giao tiếp)
- Định nghĩa: Lớp này quản lý giao tiếp giữa các hệ thống trong trạm khí tượng và các hệ thống bên ngoài (như vệ tinh, máy chủ trung tâm).

## Thuộc tính:

- connectionStatus (bool): Trạng thái kết nối.
- dataRate (float): Tốc độ truyền tải dữ liệu.
- protocol (string): Giao thức giao tiếp.
## Phương thức:

- connect(): Kết nối với các hệ thống khác.
- sendData(): Gửi dữ liệu.
- receiveData(): Nhận dữ liệu.
## Lý do cần có: 
- Hệ thống giao tiếp kết nối trạm khí tượng với các cơ sở dữ liệu trung tâm, các hệ thống xử lý hoặc các tổ chức khác. Điều này rất quan trọng khi cần chia sẻ dữ liệu khí tượng cho các cơ quan dự báo thời tiết hoặc cứu trợ.
## Hình ảnh mô tả lớp CommunicationSystem (Hệ thống Giao tiếp)

![Diagram](https://www.planttext.com/plantuml/png/LCp12K8n48JX-wjYZzf2Je9Me1MicrK2ILQoamSYLkR1acn1DAVCyVjXFg_tpi4DlUH5ChlJtahfDGaZMJtT7LheiT1lOhMg_1sCxe7EPdcqoE0ZGmDTiZ46tfh1n78WHqlrEjrije5MIt6WQuq71i_QL3IjEeNdyWK00F__0m00)
# 1.17 Users (Người dùng)
- Định nghĩa: Lớp này đại diện cho người dùng của hệ thống, có thể là các nhà nghiên cứu, kỹ thuật viên hoặc quản trị viên.

## Thuộc tính:

- userID (string): Mã ID người dùng.
- userRole (string): Vai trò của người dùng (quản trị viên, nhà nghiên cứu, kỹ thuật viên).
- accessLevel (int): Mức độ truy cập của người dùng (ví dụ: quyền xem, quyền sửa).
## Phương thức:

- viewData(): Xem dữ liệu khí tượng.
- updateSettings(): Cập nhật các thiết lập hệ thống.
- accessReports(): Truy cập các báo cáo khí tượng.
## Lý do cần có: 
- Người dùng cần có khả năng truy cập và sử dụng dữ liệu để phục vụ cho mục đích nghiên cứu, dự báo thời tiết, hoặc ra quyết định trong các tình huống khẩn cấp.

## Hình ảnh mô tả lớp DataProcessor (Xử lý Dữ liệu):

![Diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK9eSMfHiK8rbm88b1Qd5dcwM2aKbnHbvgKZn8BoSr9HHHEJarEBYtrIor9ph1GoyqeWecMPgUKkYIM96ffM2cNvcIbG4mfI4ajIWrDBIZBpqejHvI3c1AKMv1UL8AHgkG00003__mC0)

# Hình ảnh mô tả mối quan hệ giữa các lớp
![Diagram](https://www.planttext.com/plantuml/png/j9UzZjms4CTxFGKx9yM-W2edTmbYu0uuMtj8FKVDIOGfKYP7krW7hbExJcMuDf8wMwGumE-nJv1N22ZgO_cnCOmWrns76luudFdFxD_7lvvR0aD39ujdxEhf0sVoTFojPxnz-gHQHaQhXhMduw-CsjFnlMeOcTEV7phskdtwnEZp7wVZHxT3WsfO_VInABW4Qrc5ocfZsIy5Stzs_FV5TSai6Q6QyzNjeSTmVGTom98zIWqqxIIWmOQxk9OIELq3mJVVbcodHJqPMkIlg_6Bq63G8YrBxsPMv-7EQ8xMQZCJ6zYxzP99OIU8tk_1sXjgmKE3KCrMT27uP4eXTo153OIfvL6R3i9hBQW_mY3f6WavhQXeZ3OtkZbdfTQWRRMimp2E0QyomQn7dwFxa4RgvWVdFnF9SFV2UAVtQ6v1GOCBuWCGeJdSu0vb61-tEGSq6kujD64yEwq4QJEU4IBPlI3URlMDtdi2NMES5s0Q_DwZfDnRxFgAj846Psp2heyVs_ejLz035tG8w0QBzUGYIbzjCYzja8p0NSR29OAPFAMa5H1AAGYlTDSj9ROkAeMSX5ObUz1QJcRHA90L6LGDjI7T_6McFkiSDKUHXNPrjvwUSb-X8WEoEbZ2bJlp-3vFRuIbyvokWI1AyoaTlCUGvcBbkLjz9z5aKlTd16fzFWgjPaAf-VX_oBZtUvFq655o6IsK805Il8tJqklOT7QUDsSCzClNMuUAukXUpbONprVOQ-j2U3Y_170NkYZMNvt4DKgC12wdkK8rzqhGJ3ozcpPLZrWdm2y7TBqXKUMl4jytpic5gdlfR7dW5uhGF09Vz47C2saFuqiTpBcmrk9WqToXwOIrGgjOYONj9HmoTDxZLkUoFIdL1VmM7AK2nJ5CZMurn5LrzackEdcBzI2Z2_TeNESwEovf91TjiyVSXWl5MGqFljJ24IFMZ9owvElv2-MPhyjyo0Dz7fJmnzrgTyL4hXFHlIpK_DnTxcMc5Fa2vqKLZuNwEX28PJ9QLYhn5ZEAmhMfxVaZU3dvIJW5EVmdIG73sylKGNY2vFYtQXoXWHBf8Csr_7_YUszndOsT6iH9uDPUwRZ49bdsGvHG4-fEu3uzV-ZTT5aXaL1DD0TxF-vb3QscTqNnZDsUZky5UpE0ybD_8qx7tu7nvPT1CK_scqqqE9UEsXRXuhGhQK_kOjgW7QEV_oPg3-KoVr_wA1oEop5H3Lach1tG5i5Skjd4pNxqlnCrMZzx5k6KjTb4uqivFlp44feIvwjObQmR2NoSah2ifqIrLmRnYj2dWAtjwUmkRl_QfrBGj3qiYETz88n6h6aEErDy9Mj1rH9jg5o5J_yCzSW9d6nHF4TLkr-b_m000F__0m00)
