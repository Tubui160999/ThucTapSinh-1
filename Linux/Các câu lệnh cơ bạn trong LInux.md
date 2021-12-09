<a name="Các câu lệnh thao tác với linux"></a>

### I. các câu lệnh thường hay sự dụng
1. uname : kiểm tra hệ điều hành đang sử dụng
2. date : kiểm tra ngày giờ trên hệ điều hành.
3. df -h : liệt kê các thiết bị đang moun vào ổ cứng
4. free -m : để kiểm tra dung lương của ram
5. cat /proc/cpuinfo : để kiểm tra thông tin của cpu.
6. clear : để xóa trắng màn hình.
7. man + câu lệnh : Show ra giới thiệu, hướng dẫn về câu lệnh đó.
### II. Các Thao tác với một thư mục
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
15. cd : để di chuyển đến các thư mục
### III Các thao tác với file 
16. ls -a : liệt kê các file ẩn.
17. cat : để xem toàn bộ nội dụng của file đấy
18. more : để xem từng trang của file đấy
19. tail : để xem 10 dòng cuối cùng của file ấy 
  + VD Muốn xem 20 dòng cuối cùng của file test
    - tail -20 test
20. head : để xem nội dung của 10 dòng đầu tiên của file
  + VD muốn xem 20 dòng đầu tiên của file h
    - head -20 h
    Copy file 
 21.  cp : copy file 
### III. Các thao tác với trình soạn thảo vi
22. vi có hai chế độ là : Lệnh và nhập liệu
  + nhập liệu : dùng để thêm sửa xóa nội dụng của file.
  + Lệnh : dùng để tìm kiếm, lưu file, thoát khỏi file ...
23. vi : để tạo 1 trình soạn thảo vi
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
### IV. Đóng gói và giải nén
24. tar -cvf : để đóng gói 1 thư mục
  + Ví Dụ : đóng gói thư mục test
    - tar -cvf test.tar test
    - cf là đóng gói
    - v là hiện thị quá trình đóng gói 
    - test.tar là tên file sau khi đóng gói
    - test là file cần đóng gói
25. tar -czf : để nén thư mục
  + Ví Dụ: nén thư mục bai1
    - tar -czf bai1.tar.gz bai1
26. tar -cjf : để nén thư mục những kích thức file sẽ nhở hơn -z những quá trình nén sẽ mất thời gian nhiều hơn.
  + Ví Dụ: nén thư mục bai2
    - tar -cjf bai2.tar.bz2 bai2 
27. tar -xf : để mở đóng gói
28. tar -xzf : để mở giải nén
29. tar -zjf : để mở giải nén
### V. Quản lý User và Group
30. cat /etc/passwd : để xem các user đang có
31. cat /etc/group : để xem các group đang có
32. groupadd : để tạo 1 group mới
  + Ví Dụ Tạo 1 group có tên là App  
    - groupadd -g 10 App
    - Với -g 10 là ID là của group vừa tạo mỗi group đều có 1 ID không giống nhau.

33. useradd : để tạo 1 user mới
  + Ví Dụ tạo 1 user có tên là vankhanh
    - useradd -g App -G DB vankhanh
    - Với -g App là group chính của user vừa tạo
    - Với -G DB là group phụ 
    - Mỗi user có thể có nhiều group.



34. Copy file 
 - cp (file_name){,.bak}


- Bạn có thể tự tạo một cái nếu bạn muốn chỉnh sửa tệp nhưng không thay đổi bản gốc. Vì vậy, thay vì di chuyển tệp ra khỏi thư mục gốc, ghi lại bằng dữ liệu mới hoặc xóa hoàn toàn, bạn có thể chỉ cần thêm `.bak` vào cuối tệp để giữ an toàn.

- *Ví dụ ta copy file `Jun.txt` su đó sử dụng lệnh `ll` để kiểm tra*

![](../images/101/cp.png)

35. Hoán đổi vị trí đứng với thư mục mẹ của nó. 
- cd -

- Ví Dụ: đang ở home và muốn đến thư mục baitap
    + cd baitap

36. Di chuyển ra thực mục mẹ của thư mục hiện tại.

- cd .. 

37. Di chuyển tới thư mục home 

- cd ~
38. Tạo ra bản sao của file 
- cp 
- Ví Dụ : copy 1 file từ file baitap
    + cp baitapcopy baitap
39. df -h :    Hiển thị không gian đĩa 


### VI. Các lệnh thường dùng để kiểm tra

40.  dmidecode -t 4 : Hiển thị thông tin CPU

41. dpkg –list | grep [search term] : Kiểm tra các phần mềm đã cài đặt có tham số grep đi kèm  

42. Hiển thị tất cả các gói đã cài đặt 
```
dpkg -list|less
```

43. Ước tính không gian đĩa tệp 
```
du -bh (đường dẫn)
```

- Ví dụ

![](../images/101/du-bh.png)

44. Hiển thị biến môi trường 

`env` hoặc `set` 

- Biến môi trường gồm có tên biến và và giá trị được gán

45. In ra biến môi trường 

- Ví dụ gán biến x=1 và in ra 

![](../images/101/in.png) 

46. Hiển thị hình ảnh
47. Ls : kiểm tra các file và thư mục đang đứng
48. Hiển thị memory đã sử dụng 
`free`

![](../images/101/free.png)

- Options : 

|Wildcards|Result|
|---|---|
|-m|hiển thị dưới dang MB|
|-g|hiển thị dưới dạng G|
|-k|hiển thị dưới dạng kilobytes|

49. Hiển thị bản ghi hệ thống 

```
gnome-system-log
```

50. In ra thông tin của cpu 

```
cat /proc/cpuinfo

```

51. In ra thông tin bộ nhớ

```
cat /proc/meminfo

```

52. In ra các thiết bị kết nối 

```
cat /proc/net/dev

```

53. In ra thông tin hiệu suất 

```
cat /proc/uptime

```

54. In ra phiên bản 

```
cat /proc/vesion

```
55. In ra nội dung của một file 

```
cat <filename>

```

56. In ra các phân vùng ổ đĩa  

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



### VII. Các lệnh dùng để tìm kiếm file và thư mục
57. Tìm kiếm 1 chuỗi trong 1 file 

```
grep <string> <filename>
```

58. Hiển thị lịch sử sử dụng các dòng lệnh

`history`

59. Hiển thị tên của máy tính 
`hostname`

![](../images/101/hostname.png)
60. Hiển thị user id và group id của user hiện đang sử dụng 

`id`

![](../images/101/id.png)

61. Hiển thị ip và netmask trên máy 

`ip a`

![](../images/101/checkip.png)

62. Hiển thị thời gian shutdown gần nhất 

```
 last -x | grep shutdown | head -1
 ```

![](../images/101/shutdown.png)


### VIII. Lệnh xóa 
63. Xoá file 

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

64. Xóa thư mục và nội dung bên trong thư mục này 

```
rmdir -rf <dir>
```

65. Xóa các file có đuôi .txt

`rm *.txt`

- Ví dụ xóa các file có đuôi .txt trong thư mục DT 

![](../images/101/rmtxt.png)

66. Xóa thư mục trống 

`rmdir <dir>`





























