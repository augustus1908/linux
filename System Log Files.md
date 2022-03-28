**Log** ghi lại liên tục các thông báo về hoạt động của cả hệ thống hoặc của các dịch vụ được triển khai trên hệ thống và file tương ứng. Log file thường là các file văn bản thông thường dưới dạng “clear text” tức là bạn có thể dễ dàng đọc được nó, vì thế có thể sử dụng các trình soạn thảo văn bản (vi, vim, nano…) hoặc các trình xem văn bản thông thường (cat, tailf, head…) là có thể xem được file log.

Các tập tin log được đặt trong thư mục **/var/log**. Bất kỳ ứng dụng khác mà sau này bạn có thể cài đặt trên hệ thống của bạn có thể sẽ tạo tập tin log của chúng tại **/var/log**. Dùng lệnh **ls -l /var/log** để xem nội dung của thư mục này.

**Vai trò của log**
- TroubleShooting trong quá trình cài đặt các service.
- Tra cứu nhanh các thông tin của hệ thống.
- Truy vết các event đã và đang xảy ra

1 số file log thông dụng trên /var/log

- /var/log/messages – Chứa dữ liệu log của hầu hết các thông báo hệ thống nói chung, bao gồm cả các thông báo trong quá trình khởi động hệ thống.
- /var/log/cron – Chứa dữ liệu log của cron deamon. Bắt đầu và dừng cron cũng như cronjob thất bại.
- /var/log/maillog hoặc /var/log/mail.log – Thông tin log từ các máy chủ mail chạy trên máy chủ.
- /var/log/wtmp – Chứa tất cả các đăng nhập và đăng xuất lịch sử.
- /var/log/btmp – Thông tin đăng nhập không thành công
- /var/run/utmp – Thông tin log trạng thái đăng nhập hiện tại của mỗi người dùng.
- /var/log/dmesg – Thư mục này có chứa thông điệp rất quan trọng về kernel ring buffer. Lệnh dmesg có thể được sử dụng để xem các tin nhắn của tập tin này.
- /var/log/secure – Thông điệp an ninh liên quan sẽ được lưu trữ ở đây. Điều này bao gồm thông điệp từ SSH daemon, mật khẩu thất bại, người dùng không tồn tại, vv

## syslog
- Syslog là một giao thức client/server là giao thức dùng để chuyển log và thông điệp đến máy nhận log. 
- Máy nhận log thường được gọi là syslogd, syslog daemon hoặc syslog server. 
- Syslog có thể gửi qua UDP hoặc TCP. Các dữ liệu được gửi dạng cleartext. Syslog dùng port 514.


### Các cấp độ facility Syslog
![](blob:https://chat.zalo.me/1301ccca-1ebb-4cb4-ba4c-f75084c749a3)
![](blob:https://chat.zalo.me/a9d413d2-5bd8-480b-b7de-f1a38f8110fd)

### Mức độ cảnh báo của Syslog
![](blob:https://chat.zalo.me/29e29a8e-87c4-4f30-af98-b71b2ba67c65)


## LogRotate
Công cụ quản lý Log files

Để tránh các file log trở nên cồng kềnh và khó kiểm soát, một hệ thống quay vòng các log file được cài đặt (a log file rotation scheme).


### Cấu hình `logrotate`
![](blob:https://chat.zalo.me/a013eb9b-bd23-499e-bed4-bb89469c3562)

## Running Job in the Future

### cron
Cron là một tiện ích giúp lập lịch chạy những dòng lệnh bên phía server để thực thi một hoặc nhiều công việc nào đó theo thời gian được lập sẵn

(Nếu ta cần chạy tasks ở phía server một cách lặp lại theo thời gian định trước nào đó thì cron sẽ hỗ trợ)

Cron là một chương trình deamon, tức là nó được chạy ngầm mãi mãi một khi nó được khởi động lên







https://news.cloud365.vn/log-ly-thuyet-tong-quan-ve-log-syslog-rsyslog/

