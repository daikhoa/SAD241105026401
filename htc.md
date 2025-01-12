
# A wilderness weather station
## 1.Thiết kế hệ thống con
### 1.1Weather Data Collection System
#### 1.1.1 Hiện thực hóa giao diện 
- Chức năng chính:
  + Thu thập dữ liệu từ các cảm biến như nhiệt độ, độ ẩm, áp suất không khí, tốc độ gió, lượng mưa, ánh sáng mặt trời.
  
- Thành phần:
  + Các cảm biến (Sensors): Nhiệt độ, độ ẩm, áp suất, tốc độ gió, lượng mưa, v.v.
  
- Liên kết:
  + Kết nối với Hệ thống xử lý dữ liệu để gửi dữ liệu thô đến để làm sạch và xử lý.
  
![PlanText](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3XTNGM9HIMPoPa5YNec2Kd1gNd5-aP92Oh52C5TYSab-aOAIIs99ea90KNvoQd5nPbwwGd1bSKbghW9OaKi05nTNi8AkdO9BW8ALWll3tMip5L8Uxbwla9FvS7TxgK99nk4jN5mEgNaf8Ci00000__y30000)

#### Giải thích về Biểu đồ tuần tự:
- Sensors : Tự động thu thập dữ liệu thời tiết từ môi trường như nhiệt độ, độ ẩm, gió, vv... và chuyển đến Hệ thống xử lý dữ liệu



![PlanText](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK9mQbvnVf52DPS222Jdv-Ia9fUu99OaQcX2X8fJyrAW_5ekgAQGrDo2rAB4ajAYLApwaUIHjNcKvcQcP9PKOjK3aqJM49wPbn9Sa9gQWbK7N1QY1Qh6faPN5zE1ABAexa2HGhCHRggkdO8IA1G2YlAJKukByukK5AmKqX_kNfkfaF9mztg5dCo7kzjB5Keo3c_XSaZDIm45C0000F__0m00)

#### Giải thích biểu đồ lớp
- Sensor: Đây là một lớp cơ bản với hai phương thức công khai: collectData() và sendData().

- TemperatureSensor: Lớp này kế thừa từ Sensor và thêm phương thức collectTemperature().

- HumiditySensor: Lớp này cũng kế thừa từ Sensor và thêm phương thức collectHumidity().

- WindSpeedSensor: Lớp này kế thừa từ Sensor và thêm phương thức collectWindSpeed().




### 1.2 Hệ thống xử lý dữ liệu

#### 1.2.1 Hiện thực hóa giao diện 
- Chức năng chính:

  + Làm sạch và xử lý dữ liệu thô nhận từ hệ thống thu thập.
  + Phát hiện và loại bỏ các dữ liệu không hợp lệ.
  + Thành phần:

- Data Cleaning Module: Xử lý và làm sạch dữ liệu.
- Error Detection Module: Phát hiện lỗi trong dữ liệu thu thập.
- Liên kết:

  + Nhận dữ liệu từ Hệ thống thu thập dữ liệu.
  + Sau khi xử lý, dữ liệu được chuyển đến Hệ thống lưu trữ tạm thời.

![PlanText](https://www.planttext.com/plantuml/png/PD0_IWGn50RmFgVuc4eBBp25B6u66v70B5Y7R321p6H9tXIUmDhAri5QBBJQ55l4Y-G4Na5cNDT_JOgN7z_tUEzfjuWa0msTOrAH3wYkj2IZ0xWaYQLtJYkolaTx4qbt5MH4opOoa5Ls8tj2DKiHlD8n-Z0BBdwJ9WGVm3LzXiscuL-LIzzrGs-L_5kqQXbhSN8ABb3ZlAGdYtL9pt2sfDi1PF8hu-8WBl93XrYsep8_tPuq73M4oIF1JFCUhgHxonf-23ZBeuUQdldhwB9iTmDKVZdUPwnQrBZ-jyZRNNw4-svd2zslfwD-0000__y30000)

#### Giải thích về Biểu đồ tuần tự:
- WeatherDataCollectionSystem. Actor này đại diện cho hệ thống thu thập dữ liệu thời tiết.

- DataProcessor. Participant này chịu trách nhiệm xử lý dữ liệu thô.

- ErrorDetection. Participant này chịu trách nhiệm phát hiện lỗi trong dữ liệu.

- CommunicationSystem. Actor này đại diện cho hệ thống truyền thông.

  
![PlanText](https://www.planttext.com/plantuml/png/P90zIWH148NpFaMnaGPUO09PcDL8HDWJD3s5qz0_KbKjBhAHWR6HgOkncDk8mNYHFe5NaDvrODQjyDLxxolg9t_DMJH9yauPfvbXeKLVKJJ870dk5TGn3dMecwFZdT2Xe94peaWyQYoHyC-qLfEwjgPjk1xR27synSje6QVMRTjYMsnZ6CqxqX83HphNoKdbhPNQl_FaT9_KmCNmue7BnyRqq9Ny3iwM_9WES_-m3TpqmqQWh_O0hkHdUnYQjT7x5ApHDRHSiQ2VGGDjdrObFuGf4hwVXbUuA_aDtF2fvXYw-kvV0000__y30000)

#### Giải thích về Biểu đồ lớp:
- Định nghĩa các lớp:

  + DataProcessor: Đây là lớp chịu trách nhiệm xử lý dữ liệu với các phương thức công khai:

  + cleanData(): Làm sạch dữ liệu.

  + detectErrors(): Phát hiện lỗi.

  + storeData(): Lưu trữ dữ liệu.

  + DataCleaning: Đây là lớp chịu trách nhiệm làm sạch dữ liệu với phương thức công khai:

  + removeNoise(): Loại bỏ nhiễu.

  + ErrorDetection: Đây là lớp chịu trách nhiệm phát hiện lỗi với phương thức công khai:

  + detectSensorFaults(): Phát hiện lỗi cảm biến.

- Các tương tác:

  + DataProcessor -> DataCleaning : Làm sạch dữ liệu: Lớp DataProcessor gọi phương thức của lớp DataCleaning để làm sạch dữ liệu.

  + DataProcessor -> ErrorDetection : Phát hiện lỗi: Lớp DataProcessor gọi phương thức của lớp ErrorDetection để phát hiện lỗi.

  + DataProcessor -> "CommunicationSystem" : Chuyển dữ liệu đã xử lý: Lớp DataProcessor gửi dữ liệu đã xử lý đến hệ thống truyền thông (CommunicationSystem).


### 1.3 Temporary Storage System
#### 1.3.1 Hiện thực hóa giao diện 
- Chức năng chính:
  + Lưu trữ tạm thời dữ liệu trước khi truyền đến trung tâm điều khiển.
    
- Thành phần:
  + Temporary Storage Module: Lưu trữ dữ liệu tạm thời.
    
- Liên kết:
  + Nhận dữ liệu từ Hệ thống xử lý dữ liệu và chuẩn bị để gửi đến Hệ thống truyền thông.

[![PlanText](https://www.planttext.com/plantuml/png/NCynIiOm68VnFQVuqzqBECW7BRWu5D8BlEGB6cYIykODV1t5mTaZY7FHsI0E5U-H4tW5QKK7znyFF5_b_P24MB8V5Hc9ZAOZ8VGSZKqfSWDAw7er4OipRg8WQ0RhfyZ4CxH4fckxgq7_9jheVGxEaBWOeESark-arKgfhiVP1GQDSrnzlcGSQtd6w6gvp_XuM9zmgcN1kBwfGM-otUHbBOlxHskvWt2UQxaDgjtjNZsjZmRXfhukuIVuXmus7BVLRm000F__0m00)

#### -Giải thích về Biểu đồ tuần tự:
- DataProcessor. Actor này đại diện cho hệ thống xử lý dữ liệu.

- Participant này chịu trách nhiệm lưu trữ dữ liệu tạm thời.

- Actor này đại diện cho hệ thống truyền thông.


[![PlanText](https://www.planttext.com/plantuml/png/R4yx2i905Ept5A_K8XUm2848jaAym6EpX8NzXDstO10BiR3s3DR10onY4I-o9_0A4enLd79ccCyxFWjFw2XenRX2xs4dT6iTkguYwx0HS60mmfDruYTArIsMNrwZmKPCvX9Rv996ySZMIBXrbWllfMcgpfFGaEMpXXLiKkmbr2dUGSaKBm5Ur-46-nHxKCE3pJPbEPHMws0aHvBMJE7_ar8y0xdGfNWoh12c7i-o3m000F__0m00)

#### -Giải thích biểu đồ lớp
- emporaryStorage: Đây là lớp chịu trách nhiệm lưu trữ dữ liệu tạm thời với các phương thức công khai:

  + storeTemporarily(): Lưu trữ dữ liệu tạm thời.

  + manageStorageCapacity(): Quản lý dung lượng lưu trữ.

- DataProcessingSystem: Đây là hệ thống xử lý dữ liệu, tương tác với lớp TemporaryStorage.

- CommunicationSystem: Đây là hệ thống truyền thông, tương tác với lớp TemporaryStorage.





### 1.4 Remote maintenance and configuration system
#### 1.4.1 Hiện thực hóa giao diện 
- Chức năng chính:

  + Truyền tải dữ liệu từ trạm thời tiết đến trung tâm điều khiển qua vệ tinh.
  + Nhận các lệnh điều khiển hoặc cập nhật phần mềm từ trung tâm.
- Thành phần:

  + Satellite Communication Module: Truyền dữ liệu qua vệ tinh.
  + Communication Controller: Quản lý các hoạt động truyền thông.
- Liên kết:

  + Nhận cập nhật từ trung tâm điều khiển và truyền cho trung tâm.

[![PlanText](https://www.planttext.com/plantuml/png/R90nRiCm34LtdUB3Uo-GeGYWeLiN-GA48zX2RSgGwI5ZaQ6p3z2fiz6bapLaI2wY4_GAXPKsI8jknEVZ8y7FUDmEGa76hbLKYGyeIjlrFb3OmuWFL5kO_I2sAq03IgDw2k8grnCB2ksxRcHNaJZFjw3-0neIsxPEREuQafzrshC4tq9R5Xikirgfqk3k7jfWWuSKPuTTYkzeNOel8yvJYWT86FSfFhFIcJKa6vIDIyjHqAPbxl6KQqvnSigGPAF-roXDYgyEagULrj_2Arjb7pTfcUMgMezxN2E6DASFhY6EVwENqygLlCrndavlg5UrsbhUhU__0W00__y30000)

#### -Giải thích biểu đồ tuần tự

- TemporaryStorageSystem: Actor này đại diện cho hệ thống lưu trữ tạm thời.

- CommunicationSystem: Participant này chịu trách nhiệm thiết lập kết nối và truyền dữ liệu.

- Satellite: Participant này chịu trách nhiệm truyền dữ liệu từ hệ thống truyền thông đến trung tâm điều khiển và ngược lại.

- Control Center : Actor này đại diện cho trung tâm điều khiển, nơi nhận và gửi cập nhật dữ liệu.


[![PlanText](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9pVcvkQLvcSc99PdvUS6LnIMgkGZMN0WWKf-Qbk2IM96feGlX5gScfcMMfeGKfYIMf6ffSjLnGCu8JIr9pSZ9BKb4CWncJMboIc9IJMPpXd9-NbveCae9encQrhXqkqwmKN0xlp4jNA7kukrsX93ClG-78n8UxcnNI7-vUcydba9gN0l8K0000__y30000)


#### -Giải thích biểu đồ lớp

- CommunicationSystem: Đây là lớp chịu trách nhiệm về hệ thống truyền thông với các phương thức công khai:

  + sendData(): Gửi dữ liệu.
  + receiveUpdate(): Nhận cập nhật.

- SatelliteCommunication: Đây là lớp chịu trách nhiệm về giao tiếp vệ tinh với phương thức công khai:

  + establishConnection(): Thiết lập kết nối.


### 1.5 Power Management System
#### 1.5.1 Hiện thực hóa giao diện 
- Chức năng chính:

  + Quản lý và tối ưu hóa năng lượng sử dụng từ các nguồn năng lượng tái tạo như pin mặt trời, năng lượng gió.
  + Giám sát và điều phối việc tiêu thụ năng lượng giữa các thành phần hệ thống.
- Thành phần:

  + Energy Monitoring Module: Theo dõi mức năng lượng từ các nguồn.
  + Energy Optimization Module: Điều chỉnh hoạt động dựa trên mức năng lượng có sẵn.
- Liên kết:

  + Kết nối với tất cả các hệ thống khác để quản lý việc sử dụng năng lượng và đảm bảo hoạt động liên tục.

[![PlanText](https://www.planttext.com/plantuml/png/R92nQiCm54LtVSN5S_i37aeMJS7ruC6pK8mbY2KZFmVIDKFdZ1b3oD0X4EXc3HuSyX_l2_eBnLaA9VCzd0Ft9uwBZbIWlbaBfSa796Mbo5G11IcotYLG7Sf2j2gGrRPLZf18LuLwYymxIpvOLpyecJsbyfPiOp_-R38NeYpm-WQP8SNISjmreA3GSFpISBUTgx6-NpcUN2raza3p5EyyZFs_6MHuEBSlCDDf2-AujxXVUvZfMs5ZENvgT1mlM74ypxPyjfL5YkLqqGR6yt0aQCF3YDkUu-5vG2mgjvfl-WK00F__0m00)

#### -Giải thích biểu đồ tuần tự
- WeatherStation: Actor này đại diện cho trạm thời tiết.

- EnergyMonitoring. Participant này chịu trách nhiệm kiểm tra mức năng lượng.

- EnergyOptimization. Participant này chịu trách nhiệm tối ưu hóa việc sử dụng năng lượng.

[![PlanText](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9hNcfHUgLlVbvcINvHPbwwGZMN0WZaGaGWqXgQNBLSA1hy2qeoSpEh4aioy_DWMl8XOgcXnOdfgHgQ4C74v9BCiiIIL9_yye3yyjGYt_mKa5mj5nU6pRfss0otKaX_k7jjfaBsmrtxInGAIn_kMgoGdVbmTtEkGabHeaBUaUQyT8MSOniUxbwSbwx0vP2QbmBo7HS0003__mC0)


#### -Giải thích biểu đồ lớp

- EnergyMonitoring: Đây là lớp chịu trách nhiệm giám sát năng lượng với phương thức công khai:

  + monitorEnergy(): Giám sát năng lượng.

- EnergyOptimization: Đây là lớp chịu trách nhiệm tối ưu hóa năng lượng với các phương thức công khai:

  + optimizeUsage(): Tối ưu hóa việc sử dụng năng lượng.

  + activateLowPowerMode(): Kích hoạt chế độ năng lượng thấp.



### 1.6 Remote Maintenance System
#### 1.6.1 Hiện thực hóa giao diện 



  + Giám sát hoạt động của các hệ thống khác và thực hiện khôi phục hoặc gửi thông báo lỗi về trung tâm điều khiển qua Hệ thống truyền thông.
[![PlanText]()

#### -Giải thích biểu đồ tuần tự











