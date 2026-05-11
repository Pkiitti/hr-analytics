# HR Analytics Dashboard: Phân Tích Nguồn Nhân Lực và Tỷ Lệ Nghỉ Việc

## 1. Tổng Quan Dự Án
Dự án này là một Dashboard phân tích nhân sự toàn diện, được thiết kế để giúp ban Giám đốc và bộ phận Nhân sự (HR) theo dõi tình hình tuyển dụng, biến động nhân sự, và đặc biệt là phân tích sâu về tỷ lệ nhân viên nghỉ việc. Từ đó, doanh nghiệp có thể đưa ra các chiến lược giữ chân nhân tài và tối ưu hóa nguồn lực hiệu quả.

<img width="1313" height="732" alt="image" src="https://github.com/user-attachments/assets/5f891b25-c8b6-4031-9cb6-a697584957dc" />


## 2. Vấn Đề Kinh Doanh
Trong quá trình phân tích, các insight rút ra được là:
- Tỷ lệ nghỉ việc ở năm 2021 là 1 người và tăng mạnh đến 2024 với 26 người và giảm còn 9 ở năm kế tiếp
- Phòng ban Sản Xuất đang có tỉ lệ biến động cao nhất với 35 người nghỉ việc từ năm 2021 đến 2025
- Hầu hết ở các phòng ban vấn đề thu nhập là lý do chủ yếu khiến người ta nghỉ việc, có đến 18/60 người cho rằng như vậy

## 3. Tính Năng Chính Của Dashboard
- Theo Dõi KPI Tổng Quan: Hiển thị nhanh Tổng số nhân viên đang còn làm, Số lượng tuyển mới, Số lượng nghỉ việc và Tỷ lệ nghỉ việc và lương trung bình.
- Phân Tích Theo Thời Gian: Các biểu đồ xu hướng theo dõi quá trình tuyển dụng và nghỉ việc qua từng năm, giúp phát hiện các giai đoạn biến động mạnh.
- Phân Tích Nguyên Nhân: Vấn đề thu nhập, cơ hội nghề nghiệp, áp lực là top 3 lý do khiến nhân viên nghỉ việc tại công ty.
- Phân Bổ Theo Phòng Ban: [Đánh giá chi tiết tình hình nhân sự tại Sản xuất, Kho vận, Kiểm định chất lượng, Bảo trì và Hành chính]. Phòng ban Sản xuất với số tuyển dụng cao nhất
- với 153 lượt tuyển và 35 lượt nghỉ việc trong 5 năm (2021 đến 2025) với lý do chủ yếu là vấn đề thu nhập. Phòng ban Kiểm định chất lượng với số tuyển dụng là 52 và nghỉ việc là
- 11 người trong 5 năm, lý do lớn nhất là do cơ hội nghề nghiệp của họ. Phòng ban Kho vận với số tuyển là 33 người và nghỉ việc là 4 người với lý do trải đều ở áp lực công việc
- và cơ hội nghề nghiệp. Phòng ban Hành chính với số tuyển là 19 và số nghỉ việc là 4, lý do chủ yếu tới từ thu nhập. Phòng ban Bảo trì với số tuyển là 43, số nghỉ là 6, với
- lý do chủ yếu đến từ chuyển nơi ở và cơ hội nghề nghiệp

## 4. Cấu Trúc Mô Hình Dữ Liệu
Dự án sử dụng mô hình dữ liệu chuẩn hóa (Star Schema) với 1 bảng Danh mục và 2 bảng Sự kiện:
- Bảng Danh mục Nhân viên (Dim_Employee): Chứa thông tin định danh (Mã nhân viên, Tên, Giới tính, Phòng ban, Chức danh).
- Bảng Lịch sử Tuyển dụng (Fact_Hires): Ghi nhận biến động đầu vào (Mã nhân viên, Ngày gia nhập).
- Bảng Lịch sử Nghỉ việc (Fact_Termination): Ghi nhận biến động đầu ra (Mã nhân viên, Ngày nghỉ việc, Lý do, Mức lương cơ bản cuối cùng).

## 5. Công Nghệ Sử Dụng
- Xử lý dữ liệu (ETL): Trích xuất, làm sạch và liên kết dữ liệu từ các tệp CSV rời rạc qua Python
- Mô hình hóa dữ liệu (Data Modeling): Xây dựng sơ đồ quan hệ chuẩn để tối ưu hóa hiệu suất truy vấn.
- Trực quan hóa (Data Visualization): Thiết kế giao diện tương tác, biểu đồ và các thẻ KPI qua PowerBI

## 6. Khám Phá Dữ Liệu và Đề Xuất (Key Insights)
- Khám phá 1: Tỷ lệ nghỉ việc có xu hướng cao ở bộ phận Sản xuất, với nguyên nhân chủ yếu đến từ áp lực ca kíp và khối lượng công việc.
- Khám phá 2: Vấn đề thu nhập và cơ hội nghề nghiệp là các lý do phổ biến thứ hai khiến nhân sự quyết định rời đi, ảnh hưởng đến các vị trí chuyên môn.
- Đề xuất: Đội ngũ HR cần rà soát lại chính sách phụ cấp ca làm việc cho khối Sản xuất, đồng thời xây dựng lộ trình thăng tiến rõ ràng hơn để giữ chân các nhân sự có kinh nghiệm.

## 7. Cấu Trúc Thư Mục
- /Data: Chứa 3 tệp dữ liệu gốc định dạng CSV.
- /Dashboard: Chứa tệp báo cáo trực quan chính.
- /Images: Chứa các hình ảnh minh họa cho dự án.

## 8. Hướng Dẫn Sử Dụng
1. Tải toàn bộ kho lưu trữ (repository) này về máy tính cá nhân.
2. Mở tệp báo cáo bằng công cụ phân tích dữ liệu tương ứng.
3. Cập nhật lại đường dẫn dữ liệu (Data Source) để trỏ đúng vào thư mục /Data chứa các tệp CSV.
4. Sử dụng các bộ lọc (Slicer) trên Dashboard để tương tác và xem số liệu chi tiết theo từng năm hoặc từng phòng ban.
