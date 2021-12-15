## Swap
### 1. Khái niệm về Swap
<img src="img/swap.png">

- Swap hay còn được gọi là RAM ảo được sử dụng để hỗ trợ lưu trữ dữ liệu khi bộ nhớ vật lý (RAM) đã đầy. Đôi khi SWAP cũng được dùng song song để tăng dung lượng bộ nhớ đệm.
### 2. Tại sao cần dùng Swap
- Một trong những trường hợp quan trọng cần đến Swap là khi RAM đầy.
- Swap sẽ hạn chế các sự cố liên quan đến vấn đề bảo mật thông tin, nhất là trong hệ thống điều hành Linux.
- Swap sẽ làm nhiệm vụ duy trì tất cả các hoạt động bình thường dù tốc độ có phần chậm hơn thay vì dừng cả hệ thống khiến thông tin dễ bị rò rỉ.
### 3. Khi nào cần dùng Swap
- Khi dùng một phần mềm yêu cầu hệ thống có hỗ trợ bộ nhớ Swap trong phần cài đặt (ví dụ: Oracle).
- Khi muốn hoạt động của hệ thống ổn định hơn, đặc biệt quan trọng đối với các hệ thống không có nhiều dung lượng RAM.
- Nếu bạn đang dùng Ubuntu, hệ điều hành này sẽ yêu cầu Swap cho chế độ ngủ đông.
### 4. Size Swap bao nhiêu là phù hợp
- Nếu bộ nhớ RAM của bạn thấp như 512MB hoặc 1GB thì tốt nhất là swap tối đa không nên quá dung lượng RAM.
- Nếu RAM của bạn lớn hơn 1GB và bạn muốn sử dụng chế độ ngủ đông thì các bạn nên set Swap tối thiểu là 1GB.