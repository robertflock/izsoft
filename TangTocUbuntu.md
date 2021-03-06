# Hướng dẫn tăng tốc cho Ubuntu #
#### Giảm thời gian khởi chạy ứng dụng ####

Preload là một daemon chạy nền và phân tích hành vi người dùng đồng thời theo dõi các ứng dụng được sử dụng thường xuyên. Dựa trên những phân tích này, chương trình dự đoán ứng dụng nào có thể được người dùng sử dụng tiếp theo để nạp vào bộ nhớ. Nhờ vậy, thời gian khởi động ứng dụng giảm đi.

Cài Preload trên cửa sổ lệnh (Ctrl + Alt + T) bằng cách sử dụng câu lệnh: _sudo apt-get install preload_

Ở lần khởi động máy tiếp theo, chương trình sẽ chạy tự động.


#### Xóa file tạm ####
BleachBit là bản sao cho Linux của công cụ tối ưu hệ thống CCleaner. Chương trình giải phóng không gian bằng cách giải phóng bộ đệm, xóa cookie, gỡ bỏ lược sử Internet, file tạm… BleachBit cũng có tính năng nâng cao cho phép gỡ bỏ hoàn toàn các file nhằm chặn quá trình khôi phục.

![http://i1.download123.vn/cf/images/huongnt/2/1-huong-dan-tang-toc-cho-ubuntu.jpg](http://i1.download123.vn/cf/images/huongnt/2/1-huong-dan-tang-toc-cho-ubuntu.jpg)

Cài đặt BleachBit bằng câu lệnh sau: _sudo apt-get install bleachbit_

#### Cải thiện tốc độ bằng zRam ####

zRam là một công cụ giả ổ đĩa swap bằng cách tạo một khối trong bộ nhớ có chức năng như không gian swap. Do swap ảo này được tạo trên RAM nên nó nhanh hơn ổ swap thật rất nhiều. Nếu sở hữu cấu hình hệ thống yếu với RAM thấp thì zRam sẽ thực sự hữu ích. Đây là một công cụ cần thiết cho những máy có RAM ít hơn 2GB.

#### Cài công cụ từ PPA: ####

_sudo add-apt-repository ppa:shnatsel/zram_

_sudo apt-get update_

_sudo apt-get install zramswap-enabler_

Hoặc chỉ cần tải về file .deb

#### Tăng tốc độ khởi động hệ thống qua Grub timeout ####

Mặc định thì thời hạn Grub (Grub timeout) được đặt là 10 giây tức người dùng phải đợi sau 10 giây hoặc nhấn Enter để khởi động. Nhưng, ta có thể giảm thời gian này xuống 2 giây. Điều này cho người dùng đủ thời gian khởi động vào Windows (trong trường hợp khởi động kép dual boot) hoặc truy cập chế độ phục hồi Recovery. Để thay đổi Grub timeout, sử dụng câu lệnh sau:

_sudo gedit /etc/default/grub_

Trong file cấu hình, tìm đến dòng **GRUB\_TIMEOUT=10**. Thay thế giá trị 10 bằng giá trị mong muốn. Lưu lại file sau đó chạy câu lệnh sau để cập nhật file grub:

_sudo update-grub_

Ngoài ra, còn có rất nhiều cách khác giúp cải thiện hiệu năng Ubuntu như gỡ bỏ ứng dụng không cần thiết khi khởi động, tắt các hiệu ứng hình ảnh, dọn dẹp apt-cache, sử dụng RAM hệ thông cho thư mục tmp làm tăng tốc độ tương tác I/O.