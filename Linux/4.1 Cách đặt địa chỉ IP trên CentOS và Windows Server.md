## Đổi IP Trên CentOS 7 
- Nội Dung Thực Hiện :
    + Đặt IP cho Interface ens33 Ta thấy ens33 đang nhận IP động, ta sẽ tiến hành đặt IP tĩnh. Ta sẽ đặt theo số liệu sau:
    + IP address: 192.168.26.7
    + Gateway: 192.168.26.1
    + Subnetmask: 255.255.255.0/24
    + DNS-nameserver: 8.8.8.8
#### Bước 1 : Kiểm tra mạng có sẵn 
- nmcli device 
 <img src = "img/Screenshot_2.png" >

#### Bước 2 : Cài địa chi IP 192.168.26.7 cho mạng ens33 
- nmcli connection modify ens33 ipv4.addresses 192.168.26.7/24
    + Với "connection" : là chế độ kết nối
    + Với "modify" : là chế độ sử đổi

<img src = "img/Screenshot_7.png" >
 
#### Bước 3 Đặt Địa chỉ Gateway 192.168.26.1
- nmcli connection modify ens33 ipv4.gateway 192.168.26.7
<img src = "img/Screenshot_8.png" >

#### Bước 4 Đặt địa chỉ DNS 8.8.8.8
- nmcli con mod ens33 ipv4.dns 8.8.8.8

<img src = "img/Screenshot_9.png" >

#### Bước 5 Kiểm tra lại kết quả 

<img src = "img/Screenshot_6.png" >

## Đổi Ip Windows server 2019
- Bước 1 : Kiểm tra Default Gateway

<img src = "img/f.png" >

- Bước 2 :
<img src = "img/a.png" >

- Bước 3 :
<img src = "img/b.png" >

- Bước 4 : 

<img src = "img/c.png" >

- Bước 5 : 

<img src = "img/d.png" >

- Bước 6 : 

<img src = "img/e.png" >
