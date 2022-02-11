## Chức năng của các tầng trong mô hình TCP/IP
- Một mô hình TCP/ip tiêu chuẩn bao gồm 4 lớp được chồng lên nhau, bắt đầu từ tầng thấp nhất là tầng vật lý (Physical) -> Tầng Mạng (Network) -> Tầng giao vận (Transport) và cuối cùng là Tầng ứng dụng (Application)

### Tầng 4 : Tầng Ứng dụng (Application)
- Đây là lớp giao tiếp trên cùng của mô hình. Đúng với tên gọi, tầng ứng dụng đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chat, gửi email,một số giao thức trao đổi dữ liệu : SMTP, SSH, FTP,...) Dữ liệu khi đến đây sẽ được định dạng theo kiểu Byte nối byte, cùng với đó là các thông tin định tuyến giúp xác định đường đi đúng của một gói tin.


### Tầng 3 Tầng giao vận (Transport)
- Chức năng chính của tầng 3 là xử lý vấn đề giao tiếp giữa các máy chủ trong cùng một mạng hoặc khác mạng được kết nối với nhau thông qua bộ định tuyến. Tại đây dữ liệu sẽ được phân đoạn, mỗi đoạn sẽ không bằng nhau những kích thước phải nhỏ hơn 64KB. Cấu trúc đầy đủ của một Segment lúc này là Header chứa thông tin điều khiển và sau đó là dữ liệu.
- Trong tầng này còn bao gồm 2 giao thức cốt lõi là TCP và UDP. Trong đó, TCP đảm bảo chất lượng gói tin những tiêu tốn thời gian khá lâu để kiểm tra đầy đủ thông tin từ thứ tự dữ liệu cho đến việc kiểm soát vấn đề tắt nghẽn lưu lượng dữ liệu. Trái với điều đó UDP cho thấy tốc độ truyền tải nhanh hơn những lại không đảm bảo được chất lương dữ liệu được gửi đi.


### Tầng 2 : Tầng mạng (Internet)
- Gần giống như tầng mạng của mô hình OSI. tại đây, nó cũng được định nghĩa là một giao thức chịu trách nhiệm truyền tải dữ liệu một cách logic trong mạng. Các phần đoạn dữ liệu sẽ được đóng gói (Packets) với kích thước mỗi gói phù hợp với mạng chuyển mạch mà nó dùng để truyền dữ liệu. Lúc này, các gói tin được chèn thêm phần Header chứa thông tin của tầng mạng và tiếp tục được chuyển đến tầng tiếp theo. Các giao thức chính trong tầng là IP, ICMP và ARP.

### Tầng 1 : Tầng vật lý (Physical)
- Là sự kết hợp giữa tầng Vật lý và tầng liên kết dữ liệu của mô hình OSI. Chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Tại đây, các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi dến đích đã được chỉ định ban đầu.



## II. Mô hình OSI 
### Tầng 7 : Tầng ứng dụng (Application Layer)
- Là tầng gần nhất với người dùng. Nó cung cấp phương tiện cho người dùng truy nhập các thông tin và dữ liệu trên mạng thông qua chương trình ứng dụng. Tầng này là giao diện chính để người dùng tương tác với chương trình ứng dụng, và qua đó với mạng. 

### Tầng 6 : Tầng trình diễn ( Presentation Layer)

- Tầng trình diễn biến đổi dữ liệu để cung cấp một giao diện tiêu chuẩn cho tầng ứng dụng. Nó thực hiện các tác vụ như mã hóa dữ liệu sang dạng MIME, nén dữ liệu, và các thao tác tương tác tương tự đối với biểu diễn dữ liệu theo như cách mà chuyên viên phát triển giao thức hoặc dịch vụ cho là thích hợp. 

### Tầng 5 : Tầng Phiên (Session Layer)
- Tầng phiến kiểm soát các (Phiên) hội thoại giữa các máy tính. Tầng này thiết lập, quản lý và kết thúc các kết nối giữa trình ứng dụng địa phương và trình ứng dụng ở xa. Tầng này còn hỗ trợ hoạt động song công hoặc bán song công hoặc đơn công và thiết lập các qui trình đánh dấu điểm hoàn thành giúp việc phục hồi truyền thông nhanh hơn khi có lỗi xảy ra, vì điểm đã hoàn thành đã được đánh dấu - trì hoãn, kết thúc và khỏi động lại. Mô hình Osi ủy nhiệm cho taangfnayf trách nhiệm "ngắt mạch nhẹ nhàng" các phiên giao dịch và trách nhiệm kiểm tra và phục hồi phiên đây là phần thưởng không được dùng đến trong bộ giao thức TCP/IP.

### Tầng 4 : Tầng giao vận (Transport layer)
- Tâng giao vận cung cấp dịch vụ chuyên dụng chuyển dữ liệu giữa các người dùng tại đầu cuối, nhờ đó các tầng trên không phải quan tâm đến việc cung cấp dịch vụ truyền dữ liệu đáng tin cậy và hiểu quả. Tầng giao vận kiểm soát độ tin cậy của một kết nối được cho trước. Một số giao thức có định hướng trạng thái và kết nối. Có nghĩa là tầng giao vận có thể theo dõi các gói tin và truyền lại các gói bị thất bại. Một ví dụ điển hình của giao thức tầng 4 là TCP. Tầng này là nơi các thông điệp được chuyển sang thành các gói tin TCP hoặc UDP. Ở tầng 4 địa chỉ được đánh giá là address ports. Thông qua address ports để phân biệt được ứng dụng trao đổi.


### Tầng 3: Tầng mạng (Network )
- Tầng mạng cung cấp các chức năng và qui trình cho việc truyền các chuỗi dữ liệu có độ dài đa dạng, từ mội người tới một đích, thông qua một hoặc nhiều mạng, trong khi vẫn duy trì chất lượng dịch vụ mà tầng giao vận yêu cầu. Tầng mạng thực hiện chức nâng định tuyến. Các thiết bị định tuyến (router) hoạt động tại tầng này - gửi dữ liệu ra khắp mạng mở rộng, làm cho liên mạng trở nên khả thi tầng 3 còn gọi là chuyển mạch ip. Đây là một hệ thống định bị địac chỉ logic các giá trị được chọn bởi kỹ sư mạng. Hệ thống này có cấu trúc phả hệ.

## Tầng 2 : Tầng liên kết dữ liệu 
- Tầng liên kết dữ liệu cung cấp các phương tiện có tính chức năng và quy trình để truyền dữ liệu giữa các thực thể mạng, phát hiện và có thể sửa chữa các lỗi trong tầng vật lý nếu có. Cách đánh địa chỉ mang tính vật lý, nghĩa là địa chỉ được mã hóa cứng vào trong các thẻ mạng khi chúng được sản xuất. Hệ thống xác định địa chỉ này không có đẳng cấp. 


## Tầng 1 : Tầng vậy lý (Physical)
- Tầng vật lý định nghĩa tất cả các đặc tả về điện và vật lý cho các thiết bị. Trong đó bao gồm bố trí của các chân cắm (pin), các hiệu điện thế, và các đặc tả về cáp nối (Cable). Các thiết bị tầng vật lý bao gồm Hub. bộ lắp, thiết bị tiếp nối mạng và thiết bị tiếp hợp kênh máy chủ. Chức năng và dịch vụ căn bản được thực hiện bởi tầng vật lý.

