## I. Khái niệm về config server Firewall
<img src="img/c1.png">

- CSF viết tắt của Config Server & Firewall là 1 gói ứng dụng hoạt động trên Linux như 1 Firewall được phát hành miễn phí để tăng tính bảo mật cho server (VPS và Dedicated). CSF hoạt động dựa trên iptables và tiến trình ldf để quyét các file log để phát hiện các dấu hiệu tấn công bất thường.

## II. Tác dụng CSF Firewall
- Chống DoS các loại
- Chống Scan Port
- Đưa ra các lời khuyên về việc cấu hình server (VD: Nên nâng cấp MySQL lên bản mới hơn)
- Chống BruteForce Attack vào ftp server, web server, mail server,directadmin,cPanel…
- Chống Syn Flood
- Chống Ping Flood
- Cho phép ngăn chặn truy cập từ 1 quốc gia nào đó bằng cách chỉ định Country Code chuẫn ISO
- Hỗ trợ IPv6 và IPv4
- CHo phép khóa IP tạm thời và vĩnh viễn ở tầng mạng (An toàn hơn ở tầng ứng dụng ) nên webserver ko phải mệt nhọc xử lý yêu cầu từ các IP bị cấm nữa
- Cho phép bạn chuyến hướng yêu cầu từ các IP bị khóa sang 1 file html để thông báo cho người dùng biết IP của họ bị khóa
Và rất nhiều tính năng khác, các bạn tự tìm hiểu thêm


## II. Các câu lệnh thường dùng 
- csf -h	Trợ giúp lệnh
- csf -s	Chạy firewall
- csf -f	Dừng - Flush firewall
- csf -r	Nạp lại CSF (nhất là sau khi thay đổi cấu hình, thiết lập)
- csf -l	Hiện thị các luật iptables (IP4)
- csf -p	Kiểm tra các port đang mở
- csf --lfd	với tham số [stop|start|restart|status] để điều khiện, chạy, dừng dịch vụ lfd. Dịch vụ này giám sát quá trình đăng nhập (kiểm tra xem nó có đang hoạt động csf --lfd status)
- csf --lfd	với tham số [stop|start|restart|status] để điều khiện, chạy, dừng dịch vụ lfd. Dịch vụ này giám sát quá trình đăng nhập (kiểm tra xem nó có đang hoạt động csf --lfd status)
- csf -a	Cho phép một IP truy cập, nó thêm vào danh sách /etc/csf/csf.allow, các IP liệt kê trong danh sách này mặc định được qua Firewall, tuy nhiên nó vẫn bị LFD kiểm tra. Ví dụ thêm IP 123.123.123.123 vào thì gõ csf -a 123.123.123.123
- csf -d	Cấm một IP truy cập, nó thêm vào danh sách /etc/csf/csf.deny, ví dụ csf -d 123.123.123.123
- csf -df	Gỡ một IP ra khỏi danh sách chặn csf -df 123.123.123.123
- csf -t	hiện thị danh sách ip cho phép và bị chặn tạm thời (ip tự ra khỏi danh sách sau một khoảng thời gian)
- csf -x	Tắt hoàn toàn csf và lfd
- csf -e	Kích hoạt lại csf và lfd