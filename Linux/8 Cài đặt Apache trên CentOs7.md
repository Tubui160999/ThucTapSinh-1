### Cài đặt gói cài đặt
- Bước 1 :
- `rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY*`
- `yum -y install epel-release`
<img src = "img/s1.png">

- Bước 2 : Cài đặt MySQL / MariaDB
-  `yum -y install mariadb-server mariadb`
<img src = "img/s2.png">

- Bước 3 : Cài đặt Apache 2
- `yum -y install httpd`
<img src = "img/s6.png">

- Bước 4 : Start và enable cho httpd
- `systemctl start httpd.service`
- `systemctl enable httpd.service`
<img src = "img/s3.png">

- Bước 5 : Kiểm tra firewall và stop firewall
- `systemctl start firewall`
- `systemctl stop firewall`
<img src = "img/s4.png">

- Bước 6 : kết nối IP với Apache 2
<img src = "img/s5.png">



