## I. Khái niệm 
<img src="img/k1.png">

- KVM viết tắt của Kernel Virtualization Machine, được giới thiệu là công nghệ ảo hóa phần cứng. Điều này có nghĩa là hệ điều hành chính OS mô phỏng phần cứng cho các OS khác để chạy trên đó. Ảo hóa KVM có cách hoạt động giống như người quản lý, chia sẻ các nguồn tài nguyên ổ đĩa, network, CPU một cách công bằng. Công nghệ ảo hóa KVM nguồn mở được tích hợp trong Linux.
- Công nghệ ảo hóa có thê cho bạn chuyển Linux thành ảo hóa để máy chủ trên nhiều môi trường ảo bị cô lập gọi là máy khách hoặc máy ảo VM.
- KVM là một phần của mã Linux, nó được hưởng lợi từ các tính năng, KVM sẽ được hưởng lợi từ mọi tính năng, khả năng sửa lỗi tiến bộ cập nhập mới của Linux mà không cần kỹ thuật bổ sung.
- Khi sử dụng Cloud Computing người dùng có thể sử dụng tài nguyên trực tuyến một cách nhanh chóng mà không cần phải cài đặt phức tạp.

## II. Tính năng của công nghệ KVM
1. Tính năng bảo mật
- Công nghệ KVM kết hợp với Linux giúp tăng khả năng bảo mật SELinux (Xây dựng ranh giới bảo mật quanh máy ảo). sVirt (Đẩy mạnh khả năng của SElinux, tăng bảo mật kiểm soát truy cập bắt buộc MAC dùng cho máy ảo khách, chống lỗi ghi nhãn thủ công , cách ly VM)

2. Lưu trữ
- KVM cho phép người dùng sử dụng các bộ lưu trữ được Linux hỗ trợ như: bộ lưu trữ gắn mạng NAS, địa cục bộ,... Bạn cũng có thể chia sẻ tệp để hình ảnh ảo hóa bởi nhiều máy chủ.


3. Hỗ trợ phần cứng 
- Công nghệ KVM cũng có thể sử dụng được nhiều nền tảng phần cứng được Linux hỗ trợ.

4. Quản lý bộ nhớ
- KVM VPS được hưởng các chức năng quản lý bổ nhớ của Linux, chúng hỗ trợ truy cập bộ nhớ không đồng nhất, hợp nhất kernel cùng tran. Bộ nhớ ảo hóa KVM có khả năng hoán đổi có hiệu suất tốt được chia sẻ hoặc sao lưu bởi một tệp đĩa.

5. Di chuyển công nghệ ảo hóa KVM trực tiếp
- KVM cho phép bạn di chuyển ảo hóa trực tiếp, di chuyển một chương trình ảo hóa đang chạy mà không gây ra sự gián đoạn giữa các máy chủ vật lý. KVM vẫn được bật, mọi kết nối mạng và ứng dụng vẫn hoạt động bình thường. Đồng thời trong quá trình di chuyển nó thực hiện cả các thao tác lưu trữ.

6. Hiệu suất, khả năng mở rộng
- Như đã đề cập ở các chức năng trên của ảo hóa KVM, chúng sở hữu các ưu điểm của Linux, đồng thời chúng sẽ có khả năng mở rộng giúp phù hợp để đáp ứng như cầu khi máy khách và yêu cầu truy cập tăng lên nhiều lần. Công nghệ KVM cho phép khối lượng công việc ứng dụng yêu cầu khắt khe nhất được ảo hóa và là cơ sở cho nhiều thiết lập ảo hóa doanh nghiệp.
7. Độ trễ thấp hơn
- Linux có các phần cho phép mở rộng thời gian thực tế để các ứng dụng dựa trên KVM chạy trong một chế độ trễ thấp hơn với mức độ ưu tiên tốt hơn. Và chúng cũng tiến hành phân chia các quá trình yêu cầu một khoảng thời gian dài tính toán thành các khoảng nhỏ hơn, rồi sau đó lên lịch để xử lý tương ứng.
8. Quản lý với KVM
- Thông qua KVM cho phép quản lý thủ công chương trình ảo hóa được kích hoạt từ máy trạm, không cần qua công cụ quản lý. Chức năng này thường được sử dụng bởi các doanh nghiệp lớn để quản trị nguồn tài nguyên, tăng khả năng phân tích dữ liệu, hợp lý các hoạt động.

## III. Cách thức hoạt động của KVM
<img src="img/k2.png">


- KVM chuyển đổi một nhân Linux thành một bare metal hypervisor và thêm vào đó những đặc trưng riêng của các bộ phận xử lý Intel như Intel VT-X hay AMD-V
- Khi đã trở thành một hypervisor, KVM hoàn toàn có thể setup các máy ảo với các hệ điều hành khác nhau và không phụ thuộc vào hệ điều hành của máy chủ vật lý.
- Trong kiến trúc của KVM, Virtual machine được thực hiện tương tự như là quy trình xử lý thông thường của Linux, được lập lịch hoạt động như các schediler tiêu chuẩn của Linux.
- Trên thực tế, mỗi CPU ảo hoạt động như một tiến trình xử lý của Linux. Do đó, KVM được quyền thừa hưởng những ưu điểm từ các tính năng của nhân Linux.

## IV. Ưu điểm và hạn chế của KVM
### 1. Ưu điểm của KVM
- Linh hoạt : tùy máy chủ gốc được cài đặt Linux, nhưng KVM hỗ trợ tạo máy chủ ảo có thể chạy cả Linux, Windows. Sử dụng kết hợp với QEMU, KVM có thể chạy Mac OS . KVM cũng hỗ trợ cả x86 và x86-64 system.
- Tính độc quyền cao : cấu hình từng gói VPS KVM sẽ chỉ một người sỡ hưu và toàn quyền sử dụng tài nguyên đó (CPU, RAM, Disk space...) mà không hề bị chia sẻ hay ảnh hưởng bởi các VPS khác trên cùng hệ thống.
- Độ bảo mật chắc chắn: Tích hợp các đặc điểm bảo mật của Linux như SELinux với các cơ chế bảo mật nhiều lớp, KVM bảo vệ các máy ảo tối đa và cách ly hoàn toàn.
- Tiết kiệm chi phí, độ mở rộng cao: Được phát triển trên nền tảng mã nguồn mở hoàn toàn miễn phí, được hỗ trợ từ cộng đồng và từ nhà sản xuất thiết bị, KVM ngày càng lớn mạnh và trở thành một lựa chọn hàng đầu cho doanh nghiệp với chi phí thấp, hiệu quả sử dụng cao.

### 2. Hạn chế của KVM
- Yêu cầu cao về server/máy chủ: Là công nghệ ảo hóa hoàn toàn phần cứng, VPS KVM yêu cầu cấu hình server vật lý khá cao. Thậm chí yêu cầu phải sử dụng các server của các thương hiệu lớn như IBM, Dell thì mới đảm bảo hoạt động tốt được.