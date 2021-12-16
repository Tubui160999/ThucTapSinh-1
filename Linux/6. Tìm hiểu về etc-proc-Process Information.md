## Tìm Hiểu về /etc/proc - Process Information
### 1. Hệ Thống file /proc
- Chứa các thông tin về System Process(quá trình hệ thống).
- Proc là hệ thống file ảo (pseudo file system), một hệ thống file thời gian thực (real time) và thường trú trong bộ nhớ (memory resident) để theo dõi các process đang chạy cùng với trạng thái của hệ thống.
- Proc là hệ thống file ảo bởi vì trên thực tế nó không tồn tại trong bất kì phương tiện lưu trữ nào. Nó tồn tại dựa trên bộ nhớ ảo và dữ liệu luôn thay đổi động cùng với trạgn thái của hệ thống. Hầu hết các dữ liệu trong proc FS được cập nhật liên tục để phù hợp với trạng thái hiện tại của hệ điều hành. Nội dung của proc FS có thể được đọc bởi user có quyền thích hợp, trong đó một số phần chỉ dó thể đọc bởi owner của process và root. Nếu liệt kê thư mục root (/) ra bạn sẽ thấy
<img src = "img/t1.PNG">

### 2 Nội dung thư mục /prco
- sử dụng câu lệnh ls /proc để hiện thị các thư mục trong proc
<img src = "img/t1.PNG">

- Một số nội dung và mô tả ngắn gọn: file:/proc/cmdline

    + / proc / buddyinfo : Tệp này được sử dụng chủ yếu để chẩn đoán các vấn đề phân mảnh bộ nhớ.
    + / proc / cmdline : Tệp này hiển thị các tham số được truyền cho hạt nhân tại thời điểm nó được khởi động.
    + / proc / cpuinfo : Tệp ảo này xác định loại bộ xử lý được hệ thống của bạn sử dụng.
    + / proc / crypto : Tệp này liệt kê tất cả các mật mã đã cài đặt được nhân Linux sử dụng, bao gồm các chi tiết bổ sung cho từng loại.
    + / proc / devices : Tệp này hiển thị các ký tự khác nhau và khối các thiết bị hiện được định cấu hình (không bao gồm các thiết bị có mô-đun không được tải).
    + / proc / dma : Tệp này chứa danh sách các kênh ISA DMA đã đăng ký đang được sử dụng.
    + / proc / executedomains : Tệp này liệt kê các miền thực thi hiện được hỗ trợ bởi nhân Linux, cùng với phạm vi các tính năng mà chúng hỗ trợ.
    + / proc / filesystems : Tệp này hiển thị danh sách các loại hệ thống tệp hiện được hạt nhân hỗ trợ. Cột đầu tiên cho biết liệu hệ thống tệp có được gắn trên thiết bị khối hay không. Những thứ bắt đầu bằng nodev không được gắn trên một thiết bị. Cột thứ hai liệt kê tên của hệ thống tệp được hỗ trợ. Lệnh mount chuyển qua các hệ thống tệp được liệt kê ở đây khi một hệ thống không được chỉ định làm đối số.
    + / proc / interrupts : Tệp này ghi lại số lần ngắt trên mỗi IRQ trên kiến trúc x86.
    + / proc / iomem : Tệp này hiển thị cho bạn bản đồ hiện tại của bộ nhớ hệ thống cho từng thiết bị vật lý.
    + / proc / ioports : Tệp này cung cấp danh sách các khu vực cổng hiện đã đăng ký được sử dụng để giao tiếp đầu vào hoặc đầu ra với thiết bị.
    + / proc / kcore : Tệp này đại diện cho bộ nhớ vật lý của hệ thống và được lưu trữ ở định dạng tệp lõi. Nội dung của tệp này được thiết kế để trình gỡ lỗi, chẳng hạn như gdb, và con người không thể đọc được.
    + / proc / kmsg : Tệp này được sử dụng để chứa các thông báo do hạt nhân tạo ra. Các thông báo này sau đó sẽ được các chương trình khác, chẳng hạn như / bin / dmesg, chọn.
    + / proc / loadavg : Tệp này cung cấp cái nhìn về mức trung bình tải liên quan đến cả CPU và I / O theo thời gian, cũng như dữ liệu bổ sung được sử dụng bởi thời gian hoạt động và các lệnh khác.
    + / proc / lock : Tệp này hiển thị các tệp hiện bị khóa bởi hạt nhân. Nội dung của tệp này chứa dữ liệu gỡ lỗi hạt nhân bên trong và có thể thay đổi rất nhiều, tùy thuộc vào việc sử dụng hệ thống.
    + / proc / mdstat : Tệp này chứa thông tin hiện tại cho các cấu hình RAID, nhiều đĩa.
    + / proc / meminfo : Tệp này báo cáo một lượng lớn thông tin có giá trị về việc sử dụng RAM của hệ thống.
    + / proc / modules : Tệp này hiển thị danh sách tất cả các mô-đun được tải vào hạt nhân. Hầu hết thông tin này cũng có thể được xem bằng cách sử dụng lệnh / sbin / lsmod.
#### Thư mục quy trình trong / proc
- Thư mục / proc chứa các thư mục có tên bằng số. Các thư mục này được đặt tên theo ID quy trình của chương trình và chứa thông tin về quy trình đó. Chủ sở hữu và nhóm của mỗi thư mục quy trình được đặt thành người dùng đang chạy quy trình. Mỗi thư mục quy trình chứa một số tệp bao gồm

    + cmdline: Lệnh được đưa ra khi bắt đầu quá trình
    + cwd: Một liên kết tượng trưng đến thư mục làm việc hiện tại cho quy trình
    + environ: Danh sách các biến môi trường cho quá trình
    + exe: Một liên kết tượng trưng đến tệp thực thi của quá trình này
    + fd: Thư mục chứa tất cả các bộ mô tả tệp cho một quá trình cụ thể
    + maps: Một danh sách các bản đồ bộ nhớ tới tệp thực thi và tệp thư viện được liên kết với quy trình
    + mem: Bộ nhớ do tiến trình nắm giữ (người dùng không thể đọc tệp)
    + root: Một liên kết đến thư mục gốc của quy trình
    + stat: Trạng thái của quá trình bao gồm trạng thái chạy và sử dụng bộ nhớ
    + statm: Trạng thái của bộ nhớ được sử dụng bởi quá trình
    + status: Trạng thái của quá trình ở dạng dễ đọc hơn trạng thái hoặc trạng thái