### Các Bước Cài Đặt Apache trên Ubuntu 20.4
- Đầu tiền cần kiểm tra kết nối mạng
- Tiếp theo thực hiện update apt
- `sudo apt update `
<img src = "../img/u1.png">

- `sudo apt install apache2`

<img src = "../img/u2.png">

- Kiểm tra trạng thái sau khi cài đặt hoàn thành
- `sudo service apache2 status or sudo systemctl status apache2`

<img src = "../img/u3.png">

### Kiểm tra cài đặt Apache trên Ubuntu 20.04 có thành công không.


<img src = "../img/u4.png">

### Thiết Lập Virtual Hosts
- Đầu tiên tạo thư mục cho your_domain
- `sudo mkdir -p /var/www/your_domain`
<img src = "../img/q1.png">

- Tiếp theo, cấp quyền sở hữu thư mục với user Apache www-data
- ` sudo chown -R www-data:www-data /var/www/your_domain`
<img src = "../img/q2.png">

- Tiếp theo, tạo trang index.html:
- ` sudo nano /var/www/your_domain/index.html`
<img src = "../img/q3.png">

- Nhập nội dung trang web
<img src = "../img/q7.png">

- Tiếp theo cần tạo file Virtual Hosts /etc/apache2/sites-available/your_domain.conf 
- ` sudo nano /etc/apache2/sites-available/your_domain.conf`
<img src = "../img/q4.png">

- Nội dung file Virtual Hosts
<img src = "../img/q8.png">

- Khởi động lại Apache 
- ` sudo systemctl restart apache2`
<img src = "../img/q5.png">


- Kiểm tra kết quả  
<img src = "../img/q6.png">