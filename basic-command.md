# Các câu lệnh cơ bản trong linux

1 số lưu ý:
* Sử dụng tab để tự động hoàn thành
* Sử dụng `ctrl + r search_term` để tìm kiếm các lệnh đã sử dụng trước đó, hoặc dùng mũi tên lên
* `ctrl + a` để lên đầu dòng; `ctrl + e` để xuống cuối dòng
* Chạy nhiều lệnh trong cùng 1 dòng bằng cách tách các lệnh bằng `;`
* Tìm hiểu về lệnh, ví dụ lệnh `cat` gõ `man cat`


> ls

Liệt kê nội dung thư mục
Ví dụ: `ls /applications` sẽ hiển thị tất cả các tệp và thư mục được lưu trong thư mục applications

> cd

Thay đổi, truy nhập một thư mục
Ví dụ: Thay đổi từ thư mục hiện tại thành /usr/local với `cd /usr/local`
* Đường dẫn tương đối: `cd Downloads`
* Đường dẫn tuyệt đối: `cd /home/username/Downloads`
`cd .. ` quay về thư mục mẹ
`cd - ` thay đổi trở lại thư mục làm việc trước đó
`cd ~ ` thay đổi thành thư mục chính
Nếu thư mục có khoảng trắng thì gõ: `cd 'Dir name with space'` hoặc `cd Dir\ name\ with\ space`

>sudo

Thực hiện các nhiệm vụ yêu cầu quyền quản trị hoặc quyền root.
Ví dụ: Sử dụng `sudo passwd vietanh` để thay đổi mật khẩu của người dùng "vietanh".
**sudo** để người dùng sử dụng tài khoản của họ để chạy câu lệnh hệ thống. **su** thì bắt buộc người dùng chia sẻ root password với các người dùng khác
