## Cài Đặt Php
1. Cài đặt PHP 7.3

- `sudo yum -y install http://rpms.remirepo.net/enterprise/remi-release-7.rpm`

<img src ="img/p1.png">

- `sudo yum -y install epel-release yum-utils`

<img src ="img/p2.png">

2. Tạo 1 file php với vi /var/www/html

<img src ="img/p3.png">

<img src ="img/p4.png">

3. Chạy và kiểm tra

- Lưu ý mỗi khi thay đổi ta cần thức hiện restart lại http 
<img src ="img/p5.png">
<img src ="img/p6.png">

## Cài Đặt Wordpress
1. Cài đặt Phpmyadim 
- `yum install phpMyAdmin`


2. cài đặt wget để tại Wordpress từ internet 
- Tải wget
    + `yum install wget`
<img src ="img/w1.png">
 
- Tải Wordpress
    + `wget http://wordpress.org/latest.tar.gz`
<img src ="img/w2.png">

- giải nén file wordpress
    + `tar -xzvf latest.tar.gz`
 <img src ="img/w3.png">

- Tạo Database cho wordpress
    + Tạo Database 
<img src ="img/w4.png">

+ Tạo User database
 
<img src ="img/w5.png">

- Thêm database vừa tạo vào wordpress

 <img src ="img/w6.png">

- kiểm tra kết quả
 <img src ="img/w7.png">
  <img src ="img/w8.png">