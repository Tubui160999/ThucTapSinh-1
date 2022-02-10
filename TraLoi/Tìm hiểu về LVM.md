## 1. Giới thiệu về LVM
- LVM là một phương pháp cho phép ấn định không gian đĩa cứng thành những Logical Volume khiến cho việc thay đổi kích thước trở nên dễ dàng (so với partition). Với kỹ thuật Logical Volume Manager(LVM) bạn có thể thay đổi kích thước mà không cần phải chỉnh sửa lại Partition table của OS. Điều này thực sự hữu ích với những trường hợp bạn đã sử dụng hết phần bộ nhớ còn trống của partition và muốn mở rộng dung lượng của nó,bạn chỉ cần ấn định lại dung lượng mà không cần phân vùng lại cũng không phải đối mặt với nguy cơ mất dữ liệu khi thay đổi dung lương như khi thao tác trên Partition
- Logical volume Manager (LVM): LVM là kỹ thuật quản lý việc thay đổi kích thước lưu trữ của ổ cứng. Là một phương pháp ấn định không gian ổ đĩa thành những logical volume khiến cho việc thay đổi kích thước của một phân vùng trở nên dễ dàng. Điều này thật dễ dàng khi bạn muốn quản lý công việc của mình tại riêng một phân vùng mà muốn mở rộng nó ra lớn hơn.
### Một số khái niệm liên quan.
- Physical volume : là một đĩa cứng vật lý hoặc là partition
- Volume group : là một nhóm các physical volume (Ổ đĩa ảo)


## II. Ưu điểm và nhược điểm của LVM
### 1. Ưu điểm
- Không để hệ thống bị gián đoạn hoạt động
- Không làm hỏng dịch vụ
- Có thể kết hợp với Swap
- Có thể tạo ra các vùng dung lượng lớn nhỏ tùy ý.

### 2. Nhược điểm
- Các bước thiết lập phức tạp và khó khăn hơn.
- Càng gắn nhiều đĩa cứng và thiết lập càng nhiều LVM thì hệ thống khởi động càng lâu.
- Khả năng mất dữ liệu cao khi một trong số các đĩa cứng bị hỏng
- Windows không thể nhận ra vùng dữ liệu của LVM. 


## III. Những thành phần trong LVM
- HDD : Là một thiết bị lưu trữ máy tính. Nó là loại bộ nhớ không thay đổi và không bị mất dữ liệu khi ta ngừng cung cấp nguồn điện cho chúng.
- Partition : là các phần vùng của ổ cứng. Mỗi ổ cứng có 4 partition. Trong đó bao gồm 2 loại là Primary partition và extended partition.
    + Primary partition : còn được gọi là phân vùng chính, có thể khởi động và mỗi ổ cứng chỉ có tối da 4 phân vùng này.
    + Extended partition : Hay còn được gọi là phân vùng mở rộng của ổ cứng.

## IV. Cách thức hoạt động các tầng của LVM
- Tầng đầu tiên : dard drives là tầng các disk ban đầu khi chưa chia phân vùng
- Partitions : Sau đó ta chia các disk ra thành các phân vùng nhỏ hơn
- Physical volume : từ một partitions ta sẽ tạo ra được một physical
- group volume : ta sẽ ghép nhiều physical volume thành một group volume
- Logical volume : Ta sẽ có thể tạo ra được logical volume