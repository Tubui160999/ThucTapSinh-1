### Thay đổi cách chạy từ IP sang tên miền
- Bước 1 : tạo 1 file vi có tên site01
- `vi /ect/httpd/conf.d/site01.conf`
<img src ="../img/01.png">
<img src ="../img/02.png">

- Bước 2 : Tạo 1 thư mục 
- `mkdir /ect/httpd/conf.d/var/www/site01`
<img src ="../img/03.png">
<img src ="../img/04.png">

- Bước 3 : thực hiện thay đổi file hosts trên window server.
    + Tìm đến file host và chạy bằng Notepad theo quyền admin
    + Thực hiện điền địa chỉ ip và tên miền
<img src ="../img/05.png">
<img src ="../img/06.png">

- Bước 3 : Kiểm tra và chạy theo tên miền của website
<img src ="../img/07.png">
<img src ="../img/8.png">
