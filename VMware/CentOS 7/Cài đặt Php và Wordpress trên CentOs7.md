## Cài Đặt PHP
1. Cài đặt PHP 7.3

- `sudo yum -y install http://rpms.remirepo.net/enterprise/remi-release-7.rpm`

<img src ="../img/z1.png">

- `sudo yum -y install epel-release yum-utils`

<img src ="img/h2.png">

2. Tạo 1 file php với vi /var/www/html

<img src ="img/h3.png">

<img src ="img/h4.png">

3. Chạy và kiểm tra

- Lưu ý mỗi khi thay đổi ta cần thức hiện restart lại http 
<img src ="img/h5.png">
<img src ="img/h6.png">

## Cài Đặt Wordpress
1. Cài đặt Phpmyadim 
- `yum install phpMyAdmin`
2. cài đặt wget để tải Wordpress từ internet 
- Tải wget
    + `yum install wget`
<img src ="img/w1.png">
 
- Tải Wordpress
    + `wget http://wordpress.org/latest.tar.gz`
- Giải nén file wordpress
    + `tar -xzvf latest.tar.gz`
- Tạo Database cho wordpress
    + Tạo Database 
<img src ="img/w4.png">

+ Tạo User database
 
<img src ="img/w5.png">

- Thêm database vừa tạo vào wordpress

 <img src ="img/w7.png">

- Tạo tài khoản wordpress và tạo chỉnh sửa trang web 
    + Tạo tài khoản wordperss

<img src ="img/w8.png">
   
<img src ="img/w9.png">

   + Chỉnh sửa trang web

<img src ="img/w10.png"> 
  
<img src ="img/w11.png">