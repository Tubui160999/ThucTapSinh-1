## I. Khái niệm về Openstack
<img src="img/o1.png">

- OpenStack là một ứng dụng của công nghệ ảo hóa(Virtualization). Việc ảo hóa này chính là ảo hóa các phần cứng, phần mềm, các hệ thông, hệ điều hành, chương trình vận hành, điều khiển các phần mềm đó tương tự như một máy chủ vật lý mà người ta thường gộp các tài nguyeenaor này thành một máy chủ ảo VPS.
- Nó chính là một hệ thống mã nguồn mở ảo hay là một hệ điều hành ảo cho phép người dùng có thể nghiên cứu, chỉnh sửa, quản lý thông tin của mình một các tùy ý, hiệu quả theo nhu cầu của họ.

## II. Các phần phần bên trong của Openstack
<img src="img/o2.png">

### 1. Compute Infrastructure
- Bao gồm nhiều loại nava như : nova compute, nova network, nova schedule, nova apo và nova volume.
- No-Schedule có nhiệm vụ lọc ra các thông tin cụ thể từ số lượng thông tin khổng lồ để cung cấp một cách kịp thời. No-compute với nhiệm vụ chạy các máy ảo, No-network thực hiện việc cấu hình lại các mạng ảo cho máy ảo. Cuối cùng là No-Volume sẽ tiếp nhận công việc xử lý, tạo xóa thêm hoặc bớt các volume vào instance.

### 2. Storega Infrastructure (Swift)
- Bao gồm nhiều loại Proxy node và Storage nodes. Ban đầu các proxy nodes sẽ tiếp nhận các yêu cầu xử lý và gửi về cho storage nodes, tiếp theo chính là sao lưu các mục yêu cầu dưới một account, khu lưu trữ (contrainer) hoặc vùng đối tượng (các object).
- Thông tin thêm các container sẽ thuộc sở hữu của một account (không giới hạn số lượng) và các object sẽ là các tập con bên trong container. Do đó, điều bắt buộc chính là phải có ít nhất một container bên trong account để tiến hành các thao tác update. 

### 3. Imaging service (Glance)

- Qua tên gọi có thể đoán được chức năng của phần này chính là xử lý những file ảnh của máy chủ ảo. Ngoài ra, chúng ta còn thực hiện được một số công việc quản trị khác như cập nhật thêm các tính năng vitural disk images, cài đặt các chế độ quyền riêng tư cho các hình ảnh, dễ dàng tuỳ biến việc chỉnh sửa hoặc xoá ảnh.



## III. Kiến trúc của OpenStack

### Kiến trúc tổng quan của OpenStack được chia thành 3 tầng
<img src="img/o3.png">


1. Tầg ứng dụng (Your Application) : Các ứng dụng/phần mềm sử dụng OpenStack
2. Tầng Hypervisor (Standard Hardware) : Phần ứng máy chủ đã được ảo hóa để chia sẻ cho người dùng.
3. Dịch vụ OpenStack (Openstack Shared Services) : Các thành phần cơ bản như Dashboard, Compute, Networking, API, Storage.
## IV. Mô hình
### 1. Mô hình giải pháp
<img src="img/o4.png">


- Điện toán đám mây OpenStack được các nhà cung cấp dịch vụ phát triển qua 3 giải pháp :
- IaaS (Infrastructure as a service): cung cấp/cho thuê cơ sở hạ tầng như thuê máy chủ…
- PaaS (Platform as a service): cung cấp nền tảng để phát triển ứng dụng
- SaaS (Software as a service): cung cấp khả năng truy cập phần mềm linh hoạt như HCM,CRM…


### 2. Mô hình triển khai

<img src="img/o5.png">

- Các mô hình triển khai OpenStack trên thực tế

- Private Cloud: sử dụng trong một doanh nghiệp và không chia sẻ với bất kỳ ai nằm ngoài doanh nghiệp đóng
- Public Cloud: các dịch vụ trên nền tảng điện toán đám mây được dành cho cá nhân, tổ chức cùng thuê và sử dụng chung tài nguyên
- Hybrid Cloud: mô hình lai giữa public cloud và private cloud
- Community Cloud: các dịch vụ được các công ty cùng hợp tác xây dựng và cung cấp cho cộng đồng sử dụng


### 3. Các đặc điểm nổi bật
- Với OpenStack, Cloud có khả năng phục vự và đáp ứng nhu cầu người dùng một cách toàn diện :
- Thời gian boot máy ảo, cài đặt cực kỳ nhanh chóng
Giảm tối đa thời gian downtime
- Trang dashboard quản trị dễ dàng, thân thiện với người dùng
Khả năng tự phục vụ - Khả năng truy cập hệ thống trên diện rộng
Tài nguyên được người dùng tự mua, lắp đặt và phân bổ theo nhu cầu
Khả năng co dãn, đàn hồi của tài nguyên (nâng lên - hạ xuống CPU,RAM)
Tự đo lường khả năng sử dụng dịch vụ bằng cách giám sát, dự phòng
Khả năng phục hồi và sao lưu dữ liệu hoàn toàn tự động
Tốc độ đọc dữ liệu vượt trội với ổ cứng SSD siêu tốc

