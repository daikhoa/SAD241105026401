# A wilderness weather station
## 1.Thiết kế hệ thống con
### 1.1Hệ thống thu thập và xử lý dữ liệu thời tiết
#### 1.1.1 Hiện thực hóa giao diện 

![PlanText](https://www.planttext.com/plantuml/png/T9EnQXj154Nx-OgBAXjiVu0BOo8NAKm8I92qw_6WMTYTNMRV2AjKvLgb2G4fBa828eQacY6e6E7_U5-GNmYx8cG7IStiBBnxzxnxsJzXSzrGPicLXSWaLHQ38Vld4dSv-uqP86imKgQfhAWpIxdCwymG1cyvF88qXuMPG5O6f5txxjSrfd691mvh5F4txZdyG95pU7ITsGULaLPsD6j8bQdd6mvFnuKt6MNlRILLimVJ2Otcy0d4VbLsysDLrYEgR3PHwVJOEZC1nIybjekSmzn1nwNHdMfO6R9LCLI6b1LYjphEhr9kN6ByVzyUAKwCRY-4xOB3qzdk0VRVoZDCBwONfo8rEhzA5skThPjnc9l4btJy1QahtFL34gds0EPDpsExYCyeuh94mtubTLBKFbSlG5pYzlN5WMnhrsNSbVyvJo2x3ppyC-ph3v1zZ2lPbkRNwQOxojSNjq-Kb7CigIc7EUX8noArE83rRf-eZMaMlpj8zb-xSrtlo0adXlt6GSQVfq9SAtFV_aZYBm000F__0m00](https://www.planttext.com/plantuml/png/T9AnQW9148RxVOg_LD0yW8K8MeOGK4ZQoxcumjskxCqUMbgbjamHqAG82KY4fBebMApu7li4UOMm7Y4UccPdc_dccv_vjjjEHf4caoOiYabfzBdCb6Qih6YsSSCZ4bptPndn52qCX049Nwmd67hxZcJixRr1JOhm8UmMtZuqoW9VlAODv1VvHPrLGSqsUX55rrh5F0kZMXXeC_DsBYjS4kuJiL2u2xofjsiaxejLUyzezeuOkuLxHkAMAJ9Vh6A1t2t_K2TU0vvE-gHqDE9euNA_CI0TSEIBLHgMju_ZYkHXmFGNUDn_nkpMhMB8a61rqz9olp6dHbqbIQkaooNnVvFAlPs3j94Za7jAiLkClPqR2BUKWbKHPxIkJer2J3FtPX3xukNmhYUbEQ4cVR4rYDr7dR4EbyDmGpy0003__mC0))

#### -Giải thích về Biểu đồ tuần tự:
+ Sensor thu thập dữ liệu từ môi trường như nhiệt độ, độ ẩm và truyền về WeatherSystem.

+ Hệ thống con thu thập và xử lý dữ liệu gửi dữ liệu thô tới Bộ xử lý dữ liệu để làm sạch và phát hiện lỗi.

+ Sau khi dữ liệu đã được xử lý, Bộ xử lý dữ liệu trả lại dữ liệu đã làm sạch cho hệ thống.

+ Hệ thống con thu thập và xử lý dữ liệu lưu trữ tạm thời dữ liệu vào Bộ nhớ tạm.

+ Sau khi xác nhận dữ liệu đã được lưu trữ, Hệ thống con thu thập và xử lý dữ liệu truyền dữ liệu về Trung tâm điều hành.

+ Trung tâm điều hành nhận dữ liệu và có thể yêu cầu cập nhật hệ thống hoặc các điều chỉnh cấu hình nếu cần.




![PlanText](https://www.planttext.com/plantuml/png/Z5CxQiGm4ErzYYcpXI-W8YpPf0yuIseX3Hk3B9cPMSCISh8KELAk42H_vRKXfQNtcVT6_lt-ER9eaclZ2kCqCrJeEH1y5W00fTMY5LH2jR-a4p31EJJoh4K_7AQhhsAWlwEM3wJgneBDlWgXmRh3fCB9KGtE1mLTg6qFQoaOP1xDvWkMG3rRi6ah2QGlgE0DcpQGfjjmadFGsqGnmGi5Tq8lI0fEoy-HCGMAZDT-ZAaMC0wrJrhBQ7CT2MHHqCWBKI1Uuvv2Y1AppNho_UfIzBNUd99GgCOEjvQJ9VtVSdPzOfldrcf9JcDd-VhByd5yJmgkZBnnd_Ux2xlhH_L5CCG9DmXvLfNc7S2vPGJdT3M-kr7zpdoBinodEAAtyP_w0m00__y30000)

#### -Giải thích biểu đồ lớp
+ Sensor (Cảm biến) có phương thức collectData() để thu thập dữ liệu môi trường.

+ WeatherSystem (Hệ thống con thu thập và xử lý dữ liệu) quản lý việc nhận, xử lý, lưu trữ và truyền dữ liệu. Nó có các phương thức như receiveData(), processData(), storeData() và sendData().

+ DataProcessor (Bộ xử lý dữ liệu) có các phương thức cleanData() để làm sạch dữ liệu và detectErrors() để phát hiện lỗi.

+ TemporaryStorage (Bộ nhớ tạm) lưu trữ dữ liệu tạm thời với phương thức store() để lưu và retrieve() để lấy lại dữ liệu.

+ ControlCenter (Trung tâm điều hành) nhận dữ liệu từ hệ thống và có thể yêu cầu cập nhật hoặc các điều chỉnh qua phương thức sendUpdate().


### 1.2 Hệ thống quản lý năng lượng

#### 1.2.1 Hiện thực hóa giao diện 



![PlanText](https://www.planttext.com/plantuml/png/X951IWCn58RtESNFx7k1Baf1n5L5qGk4E6G2CoyXyw9qMRo0uWKSIXUA2nUk9eYB5E-H4tW54PIsGzNru_l-zzx_4T-cBKlFeQc5L6mzYcCTShmZqFgQDEhtvnoNf0l85eTKUZq_iy6hKZZfsIZZ936Aqv3x9Q5Eh_ku4tjL-fbkU1SwCgbhqAQEVm-RMJ9ilH3RsHXDTiSOuo2GXihzoe6hz48QR0XDZWzgOFzM_Q2ZoMO_Z77kmpp71VrhsK03m_h6vBW8S5MEjmPiqcC0Lpck_bGC3zhwphvyNAPxS7gY2knptv66CoJ4jAIBhpO_0G00__y30000)

#### -Giải thích về Biểu đồ tuần tự:

+ Nguồn năng lượng cung cấp thông tin về mức năng lượng cho Giám sát năng lượng.

+ Giám sát năng lượng truyền thông tin về mức năng lượng cho Quản lý năng lượng.

+ Quản lý năng lượng điều phối tiêu thụ năng lượng dựa trên mức năng lượng hiện tại.

+ Quản lý năng lượng giám sát mức năng lượng và tình trạng của pin qua Giám sát năng lượng.


![PlanText](https://www.planttext.com/plantuml/png/R951RW8n34NtEON52XPSW4M5GDqnKYN40Q8PAqITn2FR0w8j9-kYH-8AY75eWRBzp_alJaxVFtDHpzgdrjMj5u7H6-sHeVBP1qoOTGHUO0Yha1G-7G10eXoL-3KZXyDuCcJKQKpn0orSKfO-THef5vw6IgDhwhd6ySGTtTLh02fhZZaCOajBMEG1rU8Lxh2zjjl8mgiY7zRgjPU2wYtMxxVUN_hFRlp6R44HTqoxs9GLIZbZH_nmdwDpVmysdNwzFAmnWusWF9yfmXaiYRY9sIiAxADktNt7ioE5YPjZRYvVUWO00F__0m00)

#### -Giải thích biểu đồ lớp

- Power Management (Quản lý năng lượng):

  + monitorEnergy(): Giám sát mức năng lượng.
  + optimizeEnergyConsumption(): Tối ưu hóa việc tiêu thụ năng lượng.
  + manageEnergySource(): Quản lý các nguồn năng lượng tái tạo.

  
- Energy Monitoring (Giám sát năng lượng):

  + getEnergyLevel(): Lấy thông tin mức năng lượng.
  + monitorBatteryStatus(): Giám sát tình trạng của pin.
  + checkEnergySourceStatus(): Kiểm tra tình trạng các nguồn năng lượng.
 
- Energy Source (Nguồn năng lượng):

  + provideEnergy(): Cung cấp năng lượng từ các nguồn tái tạo như mặt trời, gió.
  + reportEnergyLevel(): Báo cáo mức năng lượng hiện có.

  
### 1.3 Hệ thống con truyền thông qua vệ tinh
#### 1.3.1 Hiện thực hóa giao diện 


[![PlanText](https://www.planttext.com/plantuml/png/Z94n3e9044NxFSM_01UW82GKDdPQsAAGi75t8RWKb5IqUWCDCLR4VhUWm8lC2Ro2GGj3eeHgcfdt_iyyRUSVT9ZhGWh6s2hKiH1Snq4g9HmFmro6PPp3nUD8ff7OacbIxCbq6ehiYRFlakDXZ72nwIyxg8HCgqP7awfrNfHaAmLDfk68oDuXEDcwc2zBqlxy1bprj6n1jkKGP6kLO4UcpJu8ZImXSrEGP2ivN_o3D1qW-ESSTM1-hABXJIy0003__mC0](https://www.planttext.com/plantuml/png/Z94n2iCm34Ltdq9apmKoX43erYszW8WLCDYoiMLApzQXH-eLYjCXTQ5fHkd_zpz2p_jZI89HihCgO1Gpcu0iq4mePAqH6hrpcSsCOZmtW0aggQOgynbl55UYhDT9gGg6jjyqwE34AKU2sJFJN2BKfhPzNGmTZ9uN4zsdVpV-4f6JCm8Q1Oz55oV8cqlfRyD4h27vHQuO2NBGAEKSvv3riS9Vy6xjw5sm9FHDApKGw_BR5m000F__0m00))

#### -Giải thích về Biểu đồ tuần tự:
- SatelliteCommunication yêu cầu CommunicationLayer đảm bảo kết nối vệ tinh.
  
- CommunicationLayer xác nhận kết nối với SatelliteCommunication.
  
- SatelliteCommunication tự động truyền tải dữ liệu về CommunicationLayer.
  
- CommunicationLayer xác nhận hoàn tất việc truyền tải dữ liệu.
  
- SatelliteCommunication gửi lệnh cập nhật phần mềm cho CommunicationLayer.

- CommunicationLayer xác nhận lệnh cập nhật phần mềm.

- SatelliteCommunication nhận xác nhận và hoàn tất việc cập nhật phần mềm.

[![PlanText](https://www.planttext.com/plantuml/png/V90n3i8m34Ntd29YQeTUWAbI6TcW1p2f4P4IfufT98Gu6GD7uWgeRO2Y0kl_jl_plrzl9Gj4wRnJnW6pNcn0q3ahM0NlEx86n0PQwBFIMcjaWPspVAW24PhUolB1aGZ4tieA198KqQ0zOjqsC9u3Qf9bWcyTIlAoN5tK4-0ZTmqdZAzmuYxYBDa4sjlePpeZDHEQDDOhsv6L-JtybtLOdAB-RAaelZ-mr3KZArKYDNtP3m000F__0m00)

#### -Giải thích biểu đồ lớp

- SatelliteCommunication:

  + establishConnection(): Thiết lập kết nối vệ tinh.
  + transmitData(): Truyền tải dữ liệu qua vệ tinh.
  + receiveUpdateCommand(): Nhận lệnh cập nhật phần mềm.
  + completeUpdate(): Hoàn tất việc cập nhật phần mềm.
  + CommunicationLayer:

  + ensureConnection(): Đảm bảo kết nối vệ tinh.
  + confirmConnection(): Xác nhận kết nối.
  + sendData(): Gửi dữ liệu qua vệ tinh.
  + confirmDataTransmission(): Xác nhận việc truyền tải dữ liệu.
  + receiveUpdateCommand(): Nhận lệnh cập nhật phần mềm.
  + confirmUpdate(): Xác nhận cập nhật phần mềm.

