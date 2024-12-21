# A wilderness weather station
## 1.Thiết kế hệ thống con
### 1.1Hệ thống Trạm thời tiết (WeatherStation)
#### 1.1.1 Hiện thực hóa giao diện 

![PlanText](https://www.planttext.com/plantuml/png/T5JDQXin4BxhAUROGjm7yC649hI5_X2m3pdqecxKbR1MwsfdtVfeSZ2zrQTIGY7k4d8oJMbEAueFQ_8UymHzXIB_iRAt5udLpdpppJUVzDSjZZFa5lD4CnvXQW5EX47BTNUKeKYOCAXm15rXijHcsyzJZlpCff78ijHk3tiY6NGnjJmMsoCuIpyA-veR7ejTt3EUQpmLA7ozNMINez1QeJX9auInJK5eTS9Yq8RdvEOABiZz1At8JN90MTspCAmXxvpS77Jr1uRLDUZgEe6Cobaawr27A05RQCDBHUuo0RGSDBclQeM6rTn8aEIAWJ-TG4JkbWV08Ku3lQVLBDr0FZ9KBdA8gj-F3mdL9TscHNuPKdbZO3abDmQpl3Gnw8SxSeM9MP3JK7lvHP4Rvn19Sf-Dz7kvM45zsuC29FTh_SV4X-I2AOPgzQbS81XoKmL3hn4g8ndN26zMtVPbTMzYt_H_Gc6FTgjJjnoquTN3NGvelUX8vIm1bEI-1rPX4EGqIa6kK045JULCCQ4pqSHXl-L3UowdLG6VDkvZmbomCAVL2IyTjA5dyn6viGbjJkvAUPTDLfrD_JHixjVgHy92Y0PYvzKi0YEfd9ljLbUckyzfNvdUUa3llDVMydp8gImyXpLNfB9GZ9aK1LWLIuJq_G7AYu1-pKo0qjzaAkU3evrQwziL5AYJFdfhl46k5FIbfxBpQgCF-b91GkKDrgVxXB5ZOIxy0_WF003__mC0))

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



![PlanText](https://www.planttext.com/plantuml/png/b99DJiCm48NtFiMx01V80bKg4aAmG1G4MyirZQN4YPmnIjOiMFS6hQek8yes5cAHglVm2RW2Iab_2H8ilF6yzysRqNowZrv6t92D8yO59GQubvn2QGR4IIMw_UrBJOP7Wo8Z6JF6W9GRKaAbNDEcUiQ9tyWqoHGbfZZIeAbUcqJ8B5DwTASL7IaQmOKcQHwva8onmo0uEUr08C2vTwN2qBjNHCgx5miAc-UhCiLol5fuDnEim_eRyC6x4b7zZgTwWgYUnCXyDHNXVe__y2wLTyynoF0rCQ-deeddtiGVY9shHO2hrSA2JEFV7tqvhcV8sm5OjxdDkLqr0lIj7a7uQfx-f4NRJkk8EziktVTP8C2jiGLowwiv7Sp6Ub8Fcnlx0W00__y30000)

#### -Giải thích về Biểu đồ trình tự:

+ Weather Station(Trạm Thời Tiết ) gửi dữ liệu thu thập được từ các cảm biến tới Data Processing Unit(Bộ Xử Lý Dữ Liệu).

+ Bộ Xử Lý Dữ Liệu thực hiện các bước xử lý dữ liệu bao gồm:
  
Xử lý và làm sạch dữ liệu.

Kiểm tra và xác thực dữ liệu để đảm bảo tính chính xác trước khi lưu trữ.

+ Sau khi dữ liệu đã được xử lý và xác thực, Data Processing Unit(Bộ Xử Lý Dữ Liệu) gửi dữ liệu đã xử lý tới Central Data Repository(Kho Dữ Liệu Trung Tâm) để lưu trữ.

+ Repository(Kho Dữ Liệu Trung Tâm) lưu trữ dữ liệu và cung cấp dữ liệu này cho Data Interface ( Giao Diện Dữ Liệu) khi có yêu cầu.

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














