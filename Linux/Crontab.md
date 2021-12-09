### Crontab trong Linux
- Crontab Linux là một dịch vụ giúp thực hiện các task được lên lịch sẵn, giúp cải thiện đáng kể hiệu suất làm việc.
- Cron là một cách để tạo và chạy các lệnh theo một chu kỳ xác định. Đây là tiện ích giúp lập lịch trình để chạy những dòng lệnh bên phía server nhằm thực thi một hoặc nhiều công việc nào đó theo thời gian được lập sẵn.
<img src="../jmg/cron.PNG">

#### Một số lệnh crontab thường dùng :
- crontab -e : Tạo hoặc chỉnh sửa file crontab
<img src ="../jmg/e.PNG">
- crontab -l : Hiện thị file crontab
<img src ="../jmg/l.PNG">

- crontabl -r : Xóa file crontab
<img src ="../jmg/r1.PNG">

#### 1 Số Bài Tập về Crontab
1. Cứ 23h hàng ngày in ra 10 file chiếm nhiều dung lượng nhất
- find -type f -exec du -Sh {} + | sort -rh | : Tìm kiếm 10 file chiếm nhiều dung lượng nhất
- * 23 * * *  : cứ mỗi 23h hàng ngày sẽ chạy chạy
-   * 23 * * * find -type f -exec du -Sh {} + | sort -rh | >> topfile.text : cứ mỗi 23h hàng ngày in ra 10 file chiếm nhiều dung lượng nhất vào file có tên là topfile.text
<img src = "../jmg/t1.PNG">

- Kết Quả
<img src = "../jmg/t2.PNG">

2. cứ 23h59p hàng ngày in ra 10 thư mục chiếm nhiều dung lượng nhất. 
-  du -hs * | sort -rh | head -10 : Tìm kiếm 10 thư mục chiếm nhiều dung lượng nhất
- 59 23 * * *  : cứ mỗi 23h59 hàng ngày sẽ chạy chạy
-   59 23 * * * du -hs * | sort -rh | head -10 >> topThuMuc.text : cứ mỗi 23h59 hàng ngày in ra 10 thư mục chiếm nhiều dung lượng nhất vào file có tên là topThuMuc.text
<img src = "../jmg/y1.PNG">

- Kết Quả

<img src = "../jmg/y2.PNG">


