
# A wilderness weather station
## 1.Thiết kế hệ thống con
### 1.1Hệ thống thu thập dữ liệu 
#### 1.1.1 Hiện thực hóa giao diện 
- Chức năng : Thu thập dữ liệu từ các cảm biến về nhiệt độ, độ ẩm, áp suất, tốc độ gió, lượng mưa, ánh sáng mặt trời và các thông số khác.
- Thành phần chính : Cảm biến (Sensors).
- Nhiệm vụ : Gửi thô dữ liệu tới bộ xử lý hệ thống.


![PlanText](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bT1Ob59Pd9cGM9UYK9mQbvnVX6Aa4jYIM90KNvoQZ58XWkYGa7N3gfMmKeXvE7kZGf79ZxSFJClNQ4aerIX9EFXhhK52YaFTwzNoCbykBiTBBHxRgP2IUR3NVjBa0n1CLt1Ii7zuUwrcMWw3sy1czwiKF5mzrg5dCDx5P8Iyq12kvQNSZcavgM0VC450000__y30000)

#### Giải thích về Biểu đồ tuần tự:
- Sensors : Tự động thu thập dữ liệu thời tiết từ môi trường như nhiệt độ, độ ẩm, gió, vv...
- DataProcessor : Nhận thô dữ liệu từ biến cảm biến để thực hiện lệnh cấm xử lý hoặc tiếp tục gửi đến các phần khác của hệ thống.



![PlanText](https://www.planttext.com/plantuml/png/L8z12i8m44NtESMGbGefTDk5TE49h1S8oQY1D0cPAQL8J-R28ta5QIXgTyDZ_kF_z_FL4klCG--5yPe8EWmKCpm40829tgFXasQzsqC3Ppqkjm1GGENnCYM41eYp2xV2VJIQNGm_EelLlSQBN05Zdp1h7l9YkFgekV3xq3lhUDh0qGNR9KIxeIaZqNz-5c8T86i9IXr1rbLraD_cBGQxZFq0003__mC0)

#### Giải thích biểu đồ lớp
- ClassSensor : Đại diện cho cảm biến, chức năng thu thập dữ liệu từ môi trường.
- Phương thức collectData()được sử dụng để thu thập dữ liệu thô và trả về đối tượng RawData.
- Thuộc tính sensorType(loại cảm biến) và location(vị trí cảm biến) giúp xác định loại cảm biến cũng như vị trí của nó.
- LớpRawData : Lưu trữ dữ liệu thô thu thập được từ cảm biến nhiệt độ, độ ẩm, tốc độ gió và ứng dụng.


![PlanText](https://www.planttext.com/plantuml/png/R96_QW914CRxVOgFgnJE5x0GYO6a2W6VO7CkTmTxUx8x1v6GsjhI8eM8HGg9a41Wbs1nmVUO9yWhX5CJOh2QcM_-_PZv2jk-8scfAhIG2PKMqGM7EUuvhA7h3sGSfg2CmyoaQ0qdZbI1MricohdIjYD8XuFwAmfXLKBIf5eXklxRdvG6b5LDxDTZZ3YyGESSfjL-pgKaEIYrLWdbfJdkUX20CfJJ1D60_RB0NSv-Qz0QAkDAwuuCXq3WnqEdTtvW5uEgOM6_Ea50woPh7CBdZCCyFXYmVovYr8inNCL-HJ68momvPjEyVesXTniEIvEYs6raKsmok7hH2EpV2MGvFELjWVD4dTx_4wABAmxh_8IFilfDF0hHLsRK_EiR003__mC0)


### 1.2 Hệ thống xử lý dữ liệu

#### 1.2.1 Hiện thực hóa giao diện 
![PlanText](https://www.planttext.com/plantuml/png/b5CzJyCm4DtxAqwTsg5_e4DLgNmD5Qfe1bRZM8sbn8xiYw0ZOkZ0r8a9YQWJGmKIJB5GXo3-Xty1Vm4vRL6J1W6RTVVktNilbq-pwcia2fCeR12AKa7pn9ePO63DN4m0WyIzisKClZLF479hPaaJY8O3WcGWmv1Hv5ACfnfPr8Y9GavvJ0H2WHWfIPdMKfLRP-JITSl53PRv-orNELIgGkEnA9QAgEaOfI8JLcz19LDhhWLWaB-AIQ5z8ACe4PoI7UcDEaFGwPLjG1UEhLdotJWAvaOPrkbjFK8NJbs2OdzaYwXPuYcRBI2qMLgpQdzNTJnUlrsvrORMkJLB2FEtNQhsxomqP4HiEORvGmJQPYaD_adZCsGKYy-d7TCeo5E4m8qB2Asvup-G52CkyO23M6TOmA4bRBPAWEOlxPemlCfPG1U67yy9e7AoqMPfL5p7VJdQztc-WAjDKd_AcCL4CLS-aifJHEY8QysbS2O7GMApHm4NrjnMrbXpytsLTVfhhhFsx2g2-qpuxZ_-0W00__y30000)

#### Giải thích về Biểu đồ tuần tự:
- Hệ thống thu thập dữ liệu gửi dữ liệu thô: Hệ thống thu thập dữ liệu gửi dữ liệu thô cho bộ xử lý dữ liệu.
- Bộ xử lý dữ liệu nhận và xử lý dữ liệu: Bộ xử lý dữ liệu nhận dữ liệu thô và thực hiện các bước xử lý như làm sạch dữ liệu và phát hiện lỗi.
- Ghi nhận lỗi: Nếu có lỗi trong dữ liệu, hệ thống sẽ ghi lại lỗi vào hệ thống quản lý lỗi.
- Lưu trữ tạm thời: Dữ liệu sau khi xử lý sẽ được lưu trữ tạm thời trong bộ nhớ tạm thời.
- Chuẩn bị dữ liệu để truyền: Dữ liệu đã xử lý sẽ được chuẩn bị để truyền đi.
- Gửi dữ liệu đã xử lý: Dữ liệu đã xử lý sẽ được gửi đến hệ thống truyền thông để tiếp tục xử lý hoặc truyền tải.

  
![PlanText](https://www.planttext.com/plantuml/png/p9E_JiCm4CPtFyKf2p3m0faO2cBeW4e7rYCv4Wl7jdmN5OGwCpCn8sR4JbGnb1V94_0Ao0ajJVapC_fttztvEv_VczS35WnILqOfZzab5WJ9STlSWfHjSsSBE6kR9nWl5p1gcsSOwxQvhHEuKG0A83F832CKF0ak8sONkX00-1x4sEvUZp93Q3T1JaAP78RW0g-O3-GnK9GTkJ0DQBdIpDhPJZ7VR3p1MTIjMWfLdW9A7IY52-DGUbxMbSwrN0-W3yIyhPnfcvzwedn00sfxWSOC8DVMwAAK0HHT4GjMFeKSXUAn3nGaQ-C32vzpe_n_6M51gJa5bg1jiVOmkErtCv5shxaoGl4mlVOqh2I_ZScueilVBBq34p8esbakjMSu9vaHsRubiOAj_TlVN-z52actlcQvI7xI3OUVGZ9jNnuSv77JJRVfy7QtV8IhlufycKuXEIcN3m9bpBLWskPUnnmrL-g0R1w_sGS0003__mC0)

#### Giải thích về Biểu đồ lớp:
- Data Processor (Bộ xử lý dữ liệu):

+ processData(): Phương thức này xử lý dữ liệu thô, biến đổi nó thành dữ liệu có thể sử dụng được.
+ cleanData(): Làm sạch dữ liệu, loại bỏ dữ liệu bị thiếu hoặc sai sót.
+ detectErrors(): Phát hiện lỗi trong dữ liệu (ví dụ: lỗi từ cảm biến hoặc dữ liệu không hợp lệ).
+ prepareDataForTransmission(): Chuẩn bị dữ liệu đã xử lý để gửi đi, đảm bảo rằng dữ liệu là chính xác và có thể truyền tải.
  
- Raw Data (Dữ liệu thô):

+ getData(): Trả về dữ liệu thô từ các cảm biến, bao gồm các thông số như nhiệt độ, độ ẩm, áp suất, v.v.
Processed Data (Dữ liệu đã xử lý):

+ getProcessedData(): Trả về dữ liệu đã qua xử lý, được chuẩn bị để sử dụng hoặc gửi đi.
Data Error (Lỗi dữ liệu):

+ logError(): Ghi lại thông tin về lỗi phát hiện được trong dữ liệu, giúp xác định nguyên nhân và có biện pháp khắc phục.
  
- Mối quan hệ giữa các lớp:
+ Data Processor (Bộ xử lý dữ liệu) xử lý Raw Data (Dữ liệu thô), phát hiện lỗi và tạo ra Processed Data (Dữ liệu đã xử lý).
+ Data Processor (Bộ xử lý dữ liệu) cũng có thể phát hiện và ghi lại lỗi trong Data Error (Lỗi dữ liệu) nếu có sự cố trong quá trình xử lý dữ liệu.


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
