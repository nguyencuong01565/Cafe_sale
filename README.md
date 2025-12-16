# Cafe_sale
--Phân tích dữ liệu sale từ 1 cửa hàng Cafe <br>
** Mục tiêu : Phân tích doanh thu và đưa ra các phương án cải thiện doanh thu từ tệp data sẵn có<br>
#Data set: https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training/data <br>

** Quy trình: <br>
1.Data cleaning (Excel, Power Querry) <br>
2.Exploratory Analysis (Pivot table & Charts) <br>
3.Visualization (PowerBI) <br>
4.Conclusion & Recommendation <br>

1. Data cleaning (Excel & Power Querry) <br>
*Dữ liệu gốc: 10.000 dòng* <br>

1.1 Các vấn đề: <br>
-Định dạng sai: Lẫn lộn text, number, date ở các cột <br>
-Lỗi value: Gía trị missing, error, unknown lẫn lộn <br>
-Chưa chuẩn hoá text trong 1 column: lỗi spelling, thừa space ... <br>
-Thiếu cột định dạng date theo Ngày/Tháng/Năm <br>

1.2 Cleaning <br>
-Chuyển dữ liệu sang dạng table <br>
-Check spelling, duplicate value <br>
-Chuẩn hoá định dạng text, number, date ở các cột <br>
-Chuẩn hoá định dạng text bằng Proper, Trim và Flashfill <br>
-Tách cột Transaction_time thành các cột thể hiện Day, Month, year <br>
-Xử lý lỗi value: <br>
  +Chuyển các lỗi blank, error, unknown thành giá trị duy nhất: Unknown để bảo toàn tính  <br>
  +Riêng với cột total_sale: Sử dụng power querry & group by để tìm giá trị average của mỗi Product -> Impute theo Product <br>
-Kiểm tra bằng Pivot table -> 100% lỗi đã được chuẩn hoá <br>
*Kết quả: File sạch, sẵn sàng để phân tích (Sheet Table_Cafe_new) <br>

**File sample 500 dòng: 

2. Exploratory Analysis <br>
-Doanh thu theo từng tháng trong năm 2023: Doanh thu không có sự biến động mạnh, dao động từ $6.800 - $7.200 <br>
-Top 4 doanh thu theo sản phẩm: Salad, Sandwich, Smoothie <br>
-Doanh thu theo hình thức bán: Online và Offline tương đương nhau. Tuy nhiên có khoảng 40% dữ liệu không xác định về hình thức bán (rất lớn) <br>
-Doanh thu dựa theo các ngày trong tuần: Chỉ duy nhất thứ 7 có ghi nhận doanh thu lớn hơn các ngày còn lại trong tuần (hơn 10%) <br>
-Phương thức thanh toán: Cash, Credit card, Digital wallet tương đương nhau và có 1 phần lớn dữ liệu không xác định. <br>

**Insight sơ bộ: <br>
-Top doanh thu đến từ các sản phẩm bán kèm như: salad, smoothie, sandwich <br>
-Doanh thu theo tháng tương đối ổn định, không có điểm bứt phá trong năm <br>
-Missing value tương đối lớn, ảnh hưởng đến phân tích chuyên sâu hơn  <br>






 
