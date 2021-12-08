### 1 Các Câu Lệnh Thương sự dụng
- uname : kiểm tra hệ điều hành đang sử dụng
- date : kiểm tra ngày giờ trên hệ điều hành.
- df -h : liệt kê các thiết bị đang moun vào ổ cứng
- free -m : để kiểm tra dung lương của ram
- cat /proc/cpuinfo : để kiểm tra thông tin của cpu.
- clear : để xóa trắng màn hình.
- man + câu lệnh : để xem các oftion của câu lệnh đó.
### 2 Các thao tác của 1 thư mục
- Trong hệ điều hành linux thư mục "/" là thư muc cao nhất.
- mkdri : để tạo một thư mục
- pwd : để xem đang đứng ở thư mục nào.
- ls : Liệt kê nội dung của thư mục đang đứng.
- mv : để di chuyển từ thư mục này đến thu mục khác
- du -sh : để kiểm tra dung lương của thư mục đang đứng
- VD Di chuyển 1 file từ /root/bai1/a.text đến thứ mục /roo/bai2
- mv /root/bai1/a.text /root/bai2/
  + với tham số đầu là tham số di chuyển và tham số thư 2 là tham số đến.
- rmdir : để xóa các thư mục và file rỗng
- rm -rf để xóa thư mục và file không rỗng
  + Lưu ý khi dùng rm -rf nên đến thư mục ấy.
### 3.Cách xem nội dụng của file
- ls -a : liệt kê các file ẩn.
- cat : để xem toàn bộ nội dụng của file đấy
- more : để xem từng trang của file đấy
- tail : để xem 10 dòng cuối cùng của file ấy 
  + VD Muốn xem 20 dòng cuối cùng của file test
    - tail -20 test
- head : để xem nội dung của 10 dòng đầu tiên của file
  + VD muốn xem 20 dòng đầu tiên của file h
    - head -20 h
### 4. Sử dụng trình soạn thảo "vi"
- vi có hai chế độ là : Lệnh và nhập liệu
  + nhập liệu : dùng để thêm sửa xóa nội dụng của file.
  + Lệnh : dùng để tìm kiếm, lưu file, thoát khỏi file ...
- vi : để tạo 1 trình soạn thảo vi
  + i : để bắt đầu nhập nội dụng
  + :wq : để thoát và lưu nội dung vừa nhập lại
  + :q! : để thoát và không lưu
  + shift + 4 : để về đầu dòng
  + shift + 6 : để về cuối dòng
  + u : để undo những gì vừa mới thực hiện
  + / : để tìm kiếm 
    - VD muốn tìm kiếm từ Hà Nội 
       + /Hà Nội : sẽ tìm đến từ trên xuống dưới dùng n để tìm kiếm từ đúng tiếp theo
  + :%s Tìm kiếm và thay thế
    - VD tìm kiếm tất cả từ 2 thay thế thành 3 
      + :%s/2/3/g với giá trị g là tất cả 
### 5. Đóng gói vè nén thư mục 
- Sử dụng công cụ tar
- tar -cvf : để đóng gói 1 thư mục
  + VD đóng gói thư mục test
    - tar -cvf test.tar test
    - cf là đóng gói
    - v là hiện thị quá trình đóng gói 
    - test.tar là tên file sau khi đóng gói
    - test là file cần đóng gói
- tar -czf : để nén thư mục
  + VD nén thư mục bai1
    - tar -czf bai1.tar.gz bai1
- tar -cjf : để nén thư mục những kích thức file sẽ nhở hơn -z những quá trình nén sẽ mất thời gian nhiều hơn.
  + VD nén thư mục bai2
    - tar -cjf bai2.tar.bz2 bai2 
- tar -xf : để mở đóng gói
- tar -xzf : để mở giải nén
- tar -zjf : để mở giải nén
### 6.Quản lý User và Group
 - Mỗi người dùng là một user
 - tập hợp các người dùng là 1 group
 - cat /etc/passwd : để xem các user đang có
 - cat /etc/group : để xem các group đang có
 - groupadd : để tạo 1 group mới
  + Vd Tạo 1 group có tên là App  
    - groupadd -g 10 App
    - với -g 10 là ID là của group vừa tạo mỗi group đều có 1 ID không giống nhau.
- useradd : để tạo 1 user mới
  + VD tạo 1 user có tên là vankhanh
    - useradd -g App -G DB vankhanh
    - Với -g App là group chính của user vừa tạo
    - Với -G DB là group phụ 
    - Mỗi user có thể có nhiều group.


