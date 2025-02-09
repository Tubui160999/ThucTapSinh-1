## I. Khái niệm về Vmware
<img src="img/v1.png">

- Vmware server là một sản phẩm đến từ nhà WMware, nơi chuyên cung cấp các phần mềm ảo hóa và điện toán đám mây. Được thành lập vào năm 1998, WMware hiện là công ty con của Dell Technologies. 

- Với Vmware Server, bạn có thể sử dụng nhiều máy ảo (hay còn gọi là Virtual Machine) trên cùng một máy chủ vật lý. Mỗi máy ảo có thể chạy một hệ điều hành riêng. Điều đó dẫn đến việc máy chủ của bạn có thể sử dụng nhiều hệ điều hành khác nhau như Windows, macOS, Linux,... cùng một lúc. 

- Tuy nhiên, các máy ảo trên cùng một máy chủ sẽ phải dùng chung nguồn tài nguyên như mạng hoặc RAM. Do đó, có thể nói, cấu hình máy càng khủng thì số lượng máy ảo có thể dùng càng nhiều. 

## II. Lợi ích của Vmware
- Theo Vmware, ảo hóa sẽ giải quyết các thách thức cấp bách nhất của CNTT: giảm chi phí bảo trì khi mở rộng cơ sở hạ tầng. Các tổ chức thuộc mọi quy mô đang áp dụng công nghệ ảo hóa của Vmware đã gặt hái rất nhiều lợi ích trong quá trình sử dụng, chẳng hạn như:

- Loại bỏ các công việc hành chính thông thường cho các nhân viên IT nội bộ
    + Nhiều tùy chọn sao lưu và bảo mật dữ liệu, giảm nguy cơ mất dữ liệu
    + Tăng tính hiệu quả và linh hoạt của hệ thống trung tâm dữ liệu
    + Giảm chi phí vận hành, từ đó tăng khả năng sinh lời

## III. Các tính năng của máy ảo VMware
<img src="img/v2.png">

- Máy ảo (VM) cho phép một doanh nghiệp chạy hệ điều hành hoạt động như một máy tính hoàn toàn riêng biệt trong cửa sổ ứng dụng trên máy tính để bàn. Máy ảo có thể được triển khai để đáp ứng các nhu cầu về năng lượng xử lý ở các mức độ khác nhau, để chạy phần mềm yêu cầu hệ điều hành khác hoặc để kiểm tra các ứng dụng trong môi trường an toàn.
- Máy ảo đã từng được sử dụng để ảo hóa máy chủ, cho phép các nhóm CNTT hợp nhất tài nguyên máy tính của họ và nâng cao hiệu quả. Ngoài ra, máy ảo có thể thực hiện các tác vụ cụ thể được coi là quá rủi ro để thực hiện trong môi trường máy chủ, chẳng hạn như truy cập dữ liệu bị nhiễm vi-rút hoặc kiểm tra hệ điều hành. Vì máy ảo được tách biệt với phần còn lại của hệ thống nên phần mềm bên trong máy ảo không thể giả mạo máy tính chủ.


## IV. 5 loại ảo hóa VMware
- Tất cả các thành phần của trung tâm dữ liệu truyền thống hoặc cơ sở hạ tầng CNTT ngày nay đều có thể được ảo hóa, với nhiều loại ảo hóa cụ thể khác nhau:

1. Ảo hóa phần cứng
- Khi ảo hóa phần cứng, các phiên bản ảo của máy tính và hệ điều hành (VM) được tạo và hợp nhất thành một máy chủ vật lý duy nhất.

- Một hypervisor giao tiếp trực tiếp với dung lượng ổ đĩa và CPU của máy chủ vật lý để quản lý các máy ảo. Ảo hóa phần cứng, còn được gọi là ảo hóa máy chủ, cho phép sử dụng tài nguyên phần cứng hiệu quả hơn và cho một máy chạy đồng thời các hệ điều hành khác nhau.

2. Ảo hóa phần mềm
- Ảo hóa phần mềm tạo ra một hệ thống máy tính hoàn chỉnh với phần cứng cho phép một hoặc nhiều hệ điều hành khách chạy trên một máy chủ vật lý.

- Ví dụ: hệ điều hành Android có thể chạy trên máy chủ đang sử dụng hệ điều hành Windows của Microsoft, sử dụng phần cứng giống như máy chủ.

- Ngoài ra, các ứng dụng có thể được ảo hóa và phân phối từ máy chủ đến thiết bị của người dùng cuối, chẳng hạn như máy tính xách tay hoặc điện thoại thông minh. Điều này cho phép nhân viên truy cập các ứng dụng được lưu trữ tập trung khi làm việc từ xa.

3. Ảo hóa lưu trữ
- Lưu trữ có thể được ảo hóa bằng cách hợp nhất nhiều thiết bị lưu trữ vật lý để xuất hiện như một thiết bị lưu trữ duy nhất. Các lợi ích bao gồm tăng hiệu suất và tốc độ, cân bằng tải và giảm chi phí.

- Ảo hóa lưu trữ cũng giúp lập kế hoạch khôi phục sau khi mất hoặc hỏng dữ liệu, vì dữ liệu lưu trữ ảo có thể được sao chép và nhanh chóng chuyển đến vị trí khác.

4. Ảo hóa mạng
- Nhiều mạng con có thể được tạo trên cùng một mạng vật lý bằng cách kết hợp thiết bị thành một tài nguyên mạng ảo dựa trên phần mềm duy nhất. Ảo hóa mạng cũng chia băng thông khả dụng thành nhiều kênh độc lập, mỗi kênh có thể được gán cho các máy chủ và thiết bị trong thời gian thực.

- Ưu điểm bao gồm tăng độ tin cậy, tốc độ mạng, bảo mật và giám sát việc sử dụng dữ liệu tốt hơn. Ảo hóa mạng có thể là một lựa chọn tốt cho các công ty có lượng người dùng cao luôn cần truy cập.

5. Ảo hóa máy tính để bàn
- Loại ảo hóa phổ biến này tách môi trường máy tính để bàn khỏi thiết bị vật lý và lưu trữ máy tính để bàn trên máy chủ từ xa, cho phép người dùng truy cập máy tính để bàn của họ từ mọi nơi trên mọi thiết bị.

- Ngoài khả năng truy cập dễ dàng, các lợi ích của máy tính để bàn ảo bao gồm bảo mật dữ liệu tốt hơn, tiết kiệm chi phí cho các bản cập nhật và giấy phép phần mềm cũng như dễ quản lý.

