<a name="Các câu lệnh thao tác với linux"></a>


1. uname : kiểm tra hệ điều hành đang sử dụng
2. date : kiểm tra ngày giờ trên hệ điều hành.
3. df -h : liệt kê các thiết bị đang moun vào ổ cứng
4. free -m : để kiểm tra dung lương của ram
5. cat /proc/cpuinfo : để kiểm tra thông tin của cpu.
6. clear : để xóa trắng màn hình.
7. man + câu lệnh : Show ra giới thiệu, hướng dẫn về câu lệnh đó.

8. mkdri : để tạo một thư mục
9. pwd : để xem đang đứng ở thư mục nào.
10. ls : Liệt kê nội dung của thư mục đang đứng.
11. mv : để di chuyển từ thư mục này đến thu mục khác
12. du -sh : để kiểm tra dung lương của thư mục đang đứng
    + VD Di chuyển 1 file từ /root/bai1/a.text đến thứ mục /roo/bai2
    + mv /root/bai1/a.text /root/bai2/
  + với tham số đầu là tham số di chuyển và tham số thư 2 là tham số đến.
13. rmdir : để xóa các thư mục và file rỗng
14. rm -rf để xóa thư mục và file không rỗng
  + Lưu ý khi dùng rm -rf nên đến thư mục ấy.
15. ls -a : liệt kê các file ẩn.
16. cat : để xem toàn bộ nội dụng của file đấy
17. more : để xem từng trang của file đấy
18. tail : để xem 10 dòng cuối cùng của file ấy 
  + VD Muốn xem 20 dòng cuối cùng của file test
    - tail -20 test
19. head : để xem nội dung của 10 dòng đầu tiên của file
  + VD muốn xem 20 dòng đầu tiên của file h
    - head -20 h
20. vi có hai chế độ là : Lệnh và nhập liệu
  + nhập liệu : dùng để thêm sửa xóa nội dụng của file.
  + Lệnh : dùng để tìm kiếm, lưu file, thoát khỏi file ...
21. vi : để tạo 1 trình soạn thảo vi
  + i : để bắt đầu nhập nội dụng
  + :wq : để thoát và lưu nội dung vừa nhập lại
  + :q! : để thoát và không lưu
  + shift + 4 : để về đầu dòng
  + shift + 6 : để về cuối dòng
  + u : để undo những gì vừa mới thực hiện
  + / : để tìm kiếm 
    + Ví Dụ : Muốn tìm kiếm từ Hà Nội 
       + /Hà Nội : sẽ tìm đến từ trên xuống dưới dùng n để tìm kiếm từ đúng tiếp theo
  + :%s Tìm kiếm và thay thế
    - Ví Dụ: Tìm kiếm tất cả từ 2 thay thế thành 3 
      + :%s/2/3/g với giá trị g là tất cả 
22. tar -cvf : để đóng gói 1 thư mục
  + Ví Dụ : đóng gói thư mục test
    - tar -cvf test.tar test
    - cf là đóng gói
    - v là hiện thị quá trình đóng gói 
    - test.tar là tên file sau khi đóng gói
    - test là file cần đóng gói
23. tar -czf : để nén thư mục
  + Ví Dụ: nén thư mục bai1
    - tar -czf bai1.tar.gz bai1
24. tar -cjf : để nén thư mục những kích thức file sẽ nhở hơn -z những quá trình nén sẽ mất thời gian nhiều hơn.
  + Ví Dụ: nén thư mục bai2
    - tar -cjf bai2.tar.bz2 bai2 
25. tar -xf : để mở đóng gói
26. tar -xzf : để mở giải nén
27. tar -zjf : để mở giải nén
28. cat /etc/passwd : để xem các user đang có
29. cat /etc/group : để xem các group đang có
30. groupadd : để tạo 1 group mới
  + Ví Dụ Tạo 1 group có tên là App  
    - groupadd -g 10 App
    - Với -g 10 là ID là của group vừa tạo mỗi group đều có 1 ID không giống nhau.
31. useradd : để tạo 1 user mới
  + Ví Dụ tạo 1 user có tên là vankhanh
    - useradd -g App -G DB vankhanh
    - Với -g App là group chính của user vừa tạo
    - Với -G DB là group phụ 
    - Mỗi user có thể có nhiều group.
32. Copy file 
 ```
 cp (file_name){,.bak}
 ```

- Bạn có thể tự tạo một cái nếu bạn muốn chỉnh sửa tệp nhưng không thay đổi bản gốc. Vì vậy, thay vì di chuyển tệp ra khỏi thư mục gốc, ghi lại bằng dữ liệu mới hoặc xóa hoàn toàn, bạn có thể chỉ cần thêm `.bak` vào cuối tệp để giữ an toàn.

- *Ví dụ ta copy file `Jun.txt` su đó sử dụng lệnh `ll` để kiểm tra*

![](../images/101/cp.png)

33. Hoán đổi vị trí đứng với thư mục mẹ của nó. 

`cd -`

- *Ví dụ hoán đổi vị trí của thư mục `Test` với thư mục mẹ của nó là `OanhDT`*

![](../images/101/cd-.png)

34. Di chuyển ra thực mục mẹ của thư mục hiện tại.

`cd ..`

35. Di chuyển tới thư mục home 

`cd ~`

36. Di chuyển tới thư mục home 

`cd $HOME`

37. DI chuyển tới thư mục home 

`cd `

38. Cấp full quyền cho người sở hữu.QUyền đọc và ghi cho group và user

```
chmod 755 tên_file 
```

- Ví dụ phân quyền cho file linux 

![](../images/101/chmod.png)

Trong đó r viết tắt của read(đọc),w viết tắt của write (viết),và x viết tắt của execute (thực thi).

- Options

|Wildcards|Result|
|---|---|
|-f|chặn hầu hết các thông báo lỗi|
|-c|chỉ báo cáo khi có thay đổi|
|-v|đưa ra chuẩn đoán cho mọi tệp được xử lý|
|-R|thay đổi tập tin và thư mục đệ quy|


39. Cấp quyền thực thi cho user

```
chmod a+x file_name
```

40. Thay đổi quyền sở hữu của một file hoặc thư mục.

```
chown option user:group file/folder
```

- Ví dụ : thay đổi quyền sở hữu của thư mục DT sang user oanhdt.

![](../images/101/chown.png)

41. Tạo ra bản sao của file 

```
cp (file(file)).backup
```

42. Copy file1 thành file2

```
cp (file1) (file2)
```

43. Copy thư mục và file trong đó thành thư mục khác

```
cp -r <directory1> <directory2>/
```

- Ví dụ copy thư mục `DT` và các file trong thư mục đó thành thư mục `NEW`

![](../images/101/cp-r.png)

- Options 

|Wildcards|Result|
|---|---|
|-l|tập tin liên kết cứng thay vì sao chép|
|-i|nhắc nhở trước khi ghi đè|
|-L|luôn theo các liên kết tượng trưng trong nguồn|
|-s|liên kết tượng trưng thay vì sao chép|
|-u|chỉ sao chép khi tệp SOURCE mới hơn tệp đích hoặc khi tệp đích bị thiếu|

44. Hiển thị ngày tháng của máy tính 
`date`

![](../images/101/date.png)

45. Tạo file
```
dd if=/dev/sda1 of=/root/sda1.txt
```
- Ví dụ sao lưu ổ đĩa sang file .txt
![](../images/101/dd.png)

46. Hiển thị không gian đĩa 

`df -h`

![](../images/101/df.png)

Trong đó: 
- Filesystem: tên ổ đĩa 
- Size: không gian tổng 
- Used: Không gian đã sử dụng 
- Avail: Không gian trống 
- Use: Phần trăm đã sử dụng 
- Mounted on: Được gắn trên đâu trong cây thư mục root 18. Lấy thông tin của HDH và ghi vào tệp văn bản

- Option 

|Wildcards|Result|
|---|---|
|-k | Hiển thị dung lượng cho file sử dụng|
|-l |giới hạn danh sách cho các hệ thống tập tin cục bộ|
|-i |liệt kê thông tin inode thay vì sử dụng khối|
|-t |giới hạn danh sách cho các hệ thống tệp loại TYPE|


47. Lấy thông tin của hệ điều hành và ghi vào tệp văn bản.

```
dmesg>dmesg.txt
```

- Options

    |Wildcards |Result | 
    |----------|-------|
    | -c | xóa bộ đệm vòng sau khi in|  
    | -D |Vô hiệu hóa in tin nhắn đến bàn điều khiển| 
    | -d| hiển thị thời gian delta giữa các tin nhắn được in| 
    |-e |hiển thị giờ địa phương và đồng bằng thời gian ở định dạng có thể đọc được|
    |-f |giới hạn đầu ra cho các cơ sở được xác định|
    |-L|Tô màu tin nhắn|
    | -l|giới hạn đầu ra ở các mức xác định|
    |-t|không bao giờ in dấu thời gian tin nhắn|
    | -u| không gian hiển thị thông báo không gian người dùng|
    |-w| Theo dõi chờ tin nhắn mới |

48. Hiển thị thông tin hệ thống 

`dmidecode`

- Options 

|Wildcards|Result|
|---|---|
|-d|Đọc bộ nhớ từ file thiết bị|
|-V|Hiển thị phiên bản và thoát|
|-h|Hiển thị thông tin sử dụng và thoát|
|-s|Chỉ hiển thị giá trị của chuỗi DMI được xác định bởi KEYWORD|
|-t|Chỉ hiển thị các mục của loại TYPE từ danh sách sau: bios, hệ thống, ván chân tường, khung, bộ xử lý,bộ nhớ, bộ nhớ cache, kết nối, khe cắm|

49. Hiển thị thông tin BIOS
```
dmidecode -t 0
```

![](../images/101/bios.png)

50. Hiển thị thông tin CPU 

```
dmidecode -t 4
```

51. Kiểm tra các phần mềm đã cài đặt có tham số grep đi kèm 
``` 
dpkg –list | grep [search term]
```

52. Hiển thị tất cả các gói đã cài đặt 
```
dpkg -list|less
```

53. Ước tính không gian đĩa tệp 
```
du -bh (đường dẫn)
```

- Ví dụ

![](../images/101/du-bh.png)

54. Hiển thị biến môi trường 

`env` hoặc `set` 

- Biến môi trường gồm có tên biến và và giá trị được gán

55. In ra biến môi trường 

- Ví dụ gán biến x=1 và in ra 

![](../images/101/in.png) 

55. Hiển thị hình ảnh
56. Thoát khỏi terminal

`exit`

57. Hiển thị memory đã sử dụng 
`free`

![](../images/101/free.png)

- Options : 

|Wildcards|Result|
|---|---|
|-m|hiển thị dưới dang MB|
|-g|hiển thị dưới dạng G|
|-k|hiển thị dưới dạng kilobytes|

58. Hiển thị bản ghi hệ thống 

```
gnome-system-log
```

59. Tìm kiếm 1 chuỗi trong 1 file 

```
grep <string> <filename>
```

60. Hiển thị lịch sử sử dụng các dòng lệnh

`history`

61. Hiển thị tên của máy tính 
`hostname`

![](../images/101/hostname.png)

62. Hiển thị ngày tháng năm và giờ 

```
hwclock
```

![](../images/101/clock.png)

63. Hiển thị user id và group id của user hiện đang sử dụng 

`id`

![](../images/101/id.png)

64. Hiển thị ip và netmask trên máy 

`ip a`

![](../images/101/checkip.png)

65. Hiển thị thời gian shutdown gần nhất 

```
 last -x | grep shutdown | head -1
 ```

![](../images/101/shutdown.png)

67. Logout khỏi user hiện tại 

`logout`

68. Hiển thị các file, thư mục không bị ẩn trong thư mục hiện tại.

`ls`

- Options

|Wildcards|Result|
|---|---|
|-a|hiển thị cả những file bị ẩn |
|-l|sử dụng một định dạng danh sách dài|
|-s|in kích thước được phân bổ của mỗi tệp, trong các khối|
|-t|sắp xếp theo thời gian sửa đổi, mới nhất trước|
|-S|sắp xếp theo kích thước tập tin|

69. Hiển thị quyền truy cập đối với tất cả files bên trong thư mục

```
ls -l filename
```

70. Hiển thị các câu lệnh sẵn có trong trường hợp bạn quên.

`ls /usr/bin`

71. Hiển thị các modules hiện đang load trong kernel

`lsmod`

72. show thông tin phần cứng âm thanh, video,network 

```
lspci -nv | less
```

73. Đọc hướng dẫn sử dụng của câu lệnh 

`man`

- Ví dụ đọc hướng dẫn sử dụng của lệnh ls 

![](../images/101/man.png)

74. Tạo một thư mục 

```
mkdir <dir>
```

- Ví dụ tạo một thư mục tên NEW

![](../images/101/mkdir.png)

75. Di chuyển file tới một thư mục khác 

```
mv <file> <dir>
```

- Ví dụ chuyển file 1 từ folder NEW sang folder DT

![](../images/101/mv.png)

76. Đổi tên file 1 thành file 2 

```
mv file1 file2
```

![](../images/101/mvname.png)

77. Show bảng định tuyến 

```
netstat -rn
```

78. In ra các biến môi trường 

`printenv`

79. Hiển thị những process đang chạy được thực thi bởi chính user đang sử dụng.

`ps -Af`

80. Hiển thị thư mục đang đứng 

`pwd`

![](../images/101/pwd.png)

81. Xoá file 

```
rm filename
```

- VÍ dụ xóa file *minhkma.sh* trong folder DT

![](../images/101/rmfile.png)

- Options 

|Wildcards|Result|
|---|---|
|-f| bỏ qua các tệp và đối số không tồn tại, không bao giờ nhắc|
|-i|hỏi trước khi xóa|
|-r|xóa thư mục và nội dung của chúng một cách đệ quy| 
|-v|giải thích những gì đang được thực hiện|

82. Xóa thư mục và nội dung bên trong thư mục này 

```
rmdir -rf <dir>
```

83. Xóa các file có đuôi .txt

`rm *.txt`

- Ví dụ xóa các file có đuôi .txt trong thư mục DT 

![](../images/101/rmtxt.png)

84. Xóa thư mục trống 

`rmdir <dir>`

85. Hiển thị địa chỉ gate way mặc định 

`route`

86. Shutdown now 

```
shutdown -h now
```

87. Restart now 

```
shutdown - r now
```

88. SSH đến máy tính khác 

```
ssh <username>@<IP>
```

89. Sử dụng shell với quyền root. User của bạn cần có quyền su sang user root.

`sudo -i`

90. Sử dụng shell với quyền root.Giữ nguyên biến môi trường của user

 `sudo su`

91. Nén tất cả các file và thư mục bên trong một thư mục xác định thành một file

 ```
 tar czf <filename>.txt <dir>
 ```

- Ví dụ nén tất cả các file và thư mục bên trong thư mục NEW thành file A.txt 

![](../images/101/tar.png)

92. Giải nén một file 

```
tar xzvf <filename>
```

93. Liệt kê các tiến trình đang được thực thi bằng CPU

`top`

94. Tạo một file trống 

```
touch <filename>
```

95. In ra tên của terminal bạn đang đứng.

`tty`

![](../images/101/terminal.png)

96. In ra tên nhân linux bạn đang đứng 

`uname -a`

![](../images/101/uname.png)

97. In ra kiến trúc vi sử lý mà máy bạn đang dùng

`unmae -m`

![](../images/101/-m.png)

- Options 

|Wildcards|Result|
|---|---|
|-n|in tên máy chủ nút mạng|
|-s|in tên máy chủ nút mạng|
|-v|in phiên bản kernel|
|-p| in loại bộ xử lý hoặc "không xác định"|
|-o|in ra hệ điều hành|

98. Trả về tóm tắt câu lệnh đó dùng để làm gì 

```
whatis <command>

```

- Ví dụ tóm tắt câu lệnh uname dùng để làm gì.

![](../images/101/whatis.png)

99. Trả về vị trí dduwngd của một chương trình trong hệ thống 

```
whereis <command>

```

![](../images/101/whereis.png)

100. Trả về đường dẫn của một ứng dụng

```
which <command>

```

![](../images/101/which.png)

101. In ra những người đang truy cập vào máy 

`who`

102. In ra tên mà bạn đang dùng để đăng nhập vào máy.

`whoami`

103. Ký hiệu biểu diễn thư mục home 

`~`

104. In ra thông tin của cpu 

```
cat /proc/cpuinfo

```

105. In ra thông tin bộ nhớ

```
cat /proc/meminfo

```

106. In ra các thiết bị kết nối 

```
cat /proc/net/dev

```

107. In ra thông tin hiệu suất 

```
cat /proc/uptime

```

108. In ra phiên bản 

```
cat /proc/vesion

```
109. In ra nội dung của một file 

```
cat <filename>

```

110. In ra các phân vùng ổ đĩa  

```
fdisk -l

```

|Wildcards|Result|
|---|---|
|c |chuyển cờ tương thích do|
|d |xóa một phân vùng|
|g |tạo bảng phân vùng GPT trống mới|
|l   |Danh sách các loại phân vùng đã biết
|m |in menu này|
|n |thêm một phân vùng mới|
|v|in ra phiên bản của chương trình|


111. Tìm file 

```
find / -name <filename>

```

112. Tạo một file nén đuôi .gz

```
gzip test.txt

```

![](../images/101/gz.png)

113. Giải nén một file .gz

```
gzip -d test.txt.gz

```

![](../images/101/gzip-d.png)

114. Tạo một file nén đuôi .tar

```
tar -cvf <filename>.tar file1 file2 folder1 folder2

```

![](../images/101/filetar.png)

115. Thêm mới,cập nhật nội dung cho file nén tar

``` 
tar -rvf filename.tar add_file1 add_file2


```
116. Download file từ internet 

```
wget <link>

```
117. In ra số người cuối cùng đăng nhập vào máy 
```
last -n x
```
x là số người bạn muốn in ra.

118. Hiển thị tiến trình dưới dạng tree

```
pstree
```
119. Hiển thị số giây mà hệ điều hành chạy 

```
grep time /proc/stat
```
120. Tạo một người dùng mới 

```
useradd name  
```
121. Thay đổi mật khẩu người dùng

```
passwd 
```
122. Hiển thị không gian đĩa đã được sử dụng 
```
du <option> <file>

```
- Opitons 

|Wildcards|Result|
|---|---|
|-c|hiển thị tổng số lớn|
|-x|bỏ qua các thư mục trên các hệ thống tập tin khác nhau|
|-s|cho phép chỉ hiển thị tổng cộng cho mỗi đối số|
|-0|kết thúc mỗi dòng đầu ra với 0 byte chứ không phải là một dòng mới|

123. Chấm dứt một ứng dụng 
```
kill <option> <process_name>
```
- Options

|Wildcards|Result|
|---|---|
|-s|Hiển thị cách gửi các tín hiệu đến các quy trình|
|pid|hiển thị cách sử dụng một PID với lệnh kill|
|-L|Lệnh này được sử dụng để liệt kê các tín hiệu có sẵn trong một định dạng bảng|
|l|hiển thị tất cả các tín hiệu có sẵn mà bạn có thể sử dụng|

124. Hiển thị trạng thái của file 

```
stat <options> <file_name>
```

- Options 

|Wildcards|Result|
|---|---|
|-f|hiển thị trạng thái hệ thống tập tin thay vì trạng thái tập tin|
|-c|sử dụng format chỉ định thay vì mặc định|
|-t|in thông tin ở dạng terse|

125. Sắp xếp các dòng của một tệp văn bản

```
sort <options> <file>
```
- Options 

|Wildcards|Result|
|---|---|
|-b| Bỏ qua khoảng trống ở đầu dòng|
|-r| đảo ngược thứ tự sắp xếp ban đầu|
|-n| sử dụng giá trị số để sắp xếp|
|-u|Loại bỏ các dòng lặp lại một khóa trước đó|
|-o|chỉ định tệp đầu ra|

126. Cắt một dòng và trích xuất văn bản.

```
cut <options> <file>
```
- Options 

|Wildcards|Result|
|---|---|
|-b|trích xuất các byte cụ thể|
|-c|cắt theo ký tự|

127. echo 
- Lệnh echo dùng để hiển thị đoạn văn bản lên màn hình 

```
echo <options> ...

```

- Options 

|Wildcards|Result|
|---|---|
|-t|cách ra một khoảng rộng như ta nhấn tab|
|\n|xuống dòng từ chỗ có optons \n|
|*|in ra file và thư mục như với lệnh `ls`|
|"" > <file_name>|ghi thêm thông tin vào file|






































