# Cafe_sale
--Phân tích dữ liệu sale từ 1 cửa hàng Cafe <br>
** Mục tiêu : Phân tích doanh thu và đưa ra các phương án cải thiện doanh thu từ tệp data sẵn có<br>
#Data set: https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training/data <br>
#Link file: https://drive.google.com/drive/u/1/folders/1sUm0y5YW2hWokl9rcKkZTEwX0jHdBmhM

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
  +Chuyển các lỗi blank, error, unknown thành giá trị duy nhất: Unknown để bảo toàn tính minh bạch, tránh bias dữ liệu <br>
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

3.Visualization <br>
-Dashboard: PowerBI_Visualization.jpg <br>

4.Conclusion & Recommendation <br>
-Dựa trên báo cáo về tổng doanh thu theo sản phẩm, top 3 sản phẩm có doanh thu cao nhất trong năm 2023: Salad, Sandwich, smoothie. Đây là 3 sản phẩm có lượng doanh thu vượt trội, mặc dù số lượng bán không quá chênh lệch với các sản phẩm khác. Ví dụ:  <br>
  +Coffee: số lượng bán 3.368 - Doanh thu 7.088  <br>
  +Salad: số lượng bán 3310 - Doanh thu 17.392  <br>
  +Sandwich: số lượng bán 3245 - Doanh thu 13.758  <br>
*Mặc dù không có thông tin về biên độ lợi nhuận, nếu biên độ lợi nhuận không quá chênh lệch giữa các mặt hàng thì cửa hàng nên tập trung bán các sản phẩm phụ trợ như Salad, Sandwich, smoothie bằng các chương trình combo, ưu đãi cho các dịp đặc biệt (giáng sinh, lễ, Tết ...) Tuy nhiên vì hình ảnh của cửa hàng là bán cafe vậy nên vẫn cần sự có mặt của các sản phẩm từ cafe, vd: combo sáng cafe + sandwich, combo chiều cafe + salad + sandwich ...  <br>

-Doanh thu theo từng tháng không chênh lệch quá nhiều (10%) -> Điều này chứng tỏ cửa hàng đang không có những chương trình marketing thực sự nổi bật để kéo doanh thu tăng cao đột biến vào 1 số dịp trong năm (ngày lễ tình yêu, giáng sinh, halloween, Tết dương lịch ...) hoặc đang thiếu các sản phẩm theo mùa, đặc biệt với cửa hàng đồ uống thì mùa cao điểm phải là 3 tháng nắng nóng nhất (tháng 6-8).   <br>
*Cửa hàng cần có chiến lược cụ thể cho các ngày lễ trong năm để có thể kéo doanh thu tăng đột biến. Đặc biệt là đối với mùa hè, cần đẩy mạnh marketing hoặc các combo sản phẩm dành riêng cho mùa nắng nóng. Mùa hè có thể coi là mùa cao điểm của cửa hàng đồ uống, doanh thu cần phải nổi trội hơn hẳn so với các tháng còn lại trong năm.  <br>

-Đối với doanh thu tính theo ngày: chỉ có duy nhất ngày thứ 7 trong năm là ghi nhận doanh thu cao đột biến. 
*Cần đẩy mạnh hơn nữa các chiến dịch nhắm vào cuối tuần, vì đặc trưng của cửa hàng đồ uống là cao điểm vào thứ 7 và CN. Có thể cân nhắc quảng cáo mạnh vào 3 ngày cuối tuần: thứ 6,7,CN. Với các ngày trong tuần có thể nhắm vào đối tượng take away bằng các mã coupon trên sàn TMDT. 

-Dữ liệu bị missing quá nhiều đối với trường Location (địa điểm bán hàng). Gần 40% dữ liệu ở trường này được liệt vào dạng UNKNOWN, điều này ảnh hưởng rất lớn tới việc phân tích hành vi khách hàng mua hàng Onl/Offline. 
*Bộ phận Technical cần xem xét lại phần mềm hoặc quy trình lên đơn hàng để thu thập được dữ liệu chính xác hơn.




 
