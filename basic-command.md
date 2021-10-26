# Các câu lệnh cơ bản trong linux

1 số lưu ý:
* Sử dụng tab để tự động hoàn thành
* Sử dụng `ctrl + r search_term` để tìm kiếm các lệnh đã sử dụng trước đó, hoặc dùng mũi tên lên
* `ctrl + a` để lên đầu dòng; `ctrl + e` để xuống cuối dòng
* Chạy nhiều lệnh trong cùng 1 dòng bằng cách tách các lệnh bằng `;`
* Tìm hiểu về lệnh, ví dụ lệnh `cat` gõ `man cat`



> ## **cd**

Thay đổi, truy nhập một thư mục

Ví dụ: Thay đổi từ thư mục hiện tại thành /usr/local với `cd /usr/local`

* Đường dẫn tương đối: `cd Downloads`
* Đường dẫn tuyệt đối: `cd /home/username/Downloads`

`cd .. ` quay về thư mục mẹ

`cd - ` thay đổi trở lại thư mục làm việc trước đó

`cd ~ ` thay đổi thành thư mục chính

Nếu thư mục có khoảng trắng thì gõ: `cd 'Dir name with space'` hoặc `cd Dir\ name\ with\ space`


> ## **sudo**

Thực hiện các nhiệm vụ yêu cầu quyền quản trị hoặc quyền root.

Ví dụ: Sử dụng `sudo passwd vietanh` để thay đổi mật khẩu của người dùng "vietanh".

Sudo chạy như sau:

* Khi người dùng chạy sudo, hệ thống sẽ tìm trong file /etc/sudoers để xem người dùng có quyền chạy sudo hay không.

* Nếu người dùng có quyền chạy sudo, thì việc tiếp theo cần làm là nhập mật khẩu của chính user đó.

* Giả sử mật khẩu là chính xác. Bắt đầu lệnh sau sudo, không cần nhập mật khẩu để chạy sudo với tư cách root nữa.

> ## **su**

* **su** là viết tắt của switch user.

* Có thể chuyển đổi bất kể user nào

* Chỉ cần sử dụng `su-username`và nhập mật khẩu; nhưng root thì không cần nhập mật khẩu khi chuyển sang danh tính khác với su

Có 2 định dạng: `su -l username` & `su username`

-l là viết tắt của login

Nếu không chỉ định tên user, thì root được coi là tùy chọn mặc định, vì vậy lệnh để chuyển sang root là: `su -root` hoặc `su-`, `su root` hoặc `su`.

***Lưu ý ***

**su-username** sau khi chuyển đổi user, cũng đồng thời chuyển sang môi trường làm việc của user mới. Sau khi **su username** chuyển đổi user, thư mục làm việc của user ban đầu và các thư mục biến môi trường khác không thay đổi.

**sudo** để người dùng sử dụng tài khoản của họ để chạy câu lệnh hệ thống. **su** thì bắt buộc người dùng chia sẻ root password với các người dùng khác

> ## **mv**

Đổi tên hoặc di chuyển tập tin hoặc thư mục.

Ví dụ: lệnh `mv todo.txt /home/qlarson/Documents` sẽ di chuyển "todo.txt" vào thư mục "Documents".

> ## **mkdir**

Tạo một thư mục mới

Ví dụ: `mkdir vietanh` sẽ tạo một thư mục có tên "vietanh"

> ## **rmdir**

Xóa các thư mục trống

> ## **rm**

Xóa một hoặc nhiều tệp hoặc thư mục

Ví dụ: `rm todo.txt` sẽ xóa tệp

> ## **clear**

Xóa màn hình/cửa sổ dòng lệnh để bắt đầu mới.

> ## **cat**

Hiển thị nội dung của một tập tin trên màn hình

Ví dụ: `cat todo.txt` sẽ hiển thị văn bản của "todo.txt" trên màn hình.

> ## **ls**

Liệt kê nội dung thư mục

Ví dụ: `ls /applications` sẽ hiển thị tất cả các tệp và thư mục được lưu trong thư mục applications

> ## **pwd**

Hiển thị đường dẫn cho thư mục hiện tại

> ## **locate**

Xác định vị trí một tập tin cụ thể.

Ví dụ: `locate -i vacuum*mop` lệnh sẽ tìm kiếm bất kỳ tệp nào chứa từ "vacuum" và "mop". Lệnh `-i` làm cho trường hợp tìm kiếm không phân biệt chữ hoa và chữ thường.

> ## **cp**

Sao chép tập tin và thư mục.

Ví dụ: lệnh `cp todo.txt /home/qlarson/Documents` sẽ tạo một bản sao của "todo.txt" vào thư mục "Documents"

> ## **alias**

Tạo một bí danh cho các lệnh Linux.

Ví dụ: `alias search=grep` sẽ cho phép bạn sử dụng search thay vì grep

> ## **find**

Tìm kiếm các tập tin phù hợp với một mẫu được cung cấp. Lệnh này là để tìm kiếm các tệp và thư mục bằng cách sử dụng các bộ lọc như tên, kích thước, thời gian truy cập và thời gian sửa đổi. 

Ví dụ: `find /home/ -name todo.txt` sẽ tìm kiếm một tệp có tên "todo.txt" trong thư mục chính và các thư mục con của nó

> ## **grep**

Tìm kiếm tệp hoặc đầu ra cho một chuỗi hoặc biểu thức cụ thể. Lệnh này tìm kiếm các dòng chứa một mẫu đã chỉ định và theo mặc định, ghi chúng vào đầu ra tiêu chuẩn.

Ví dụ: `grep run todo.txt` sẽ tìm kiếm từ "run" trong tệp "todo.txt". Các dòng có chứa "run" sẽ được hiển thị.

> ## **history**

Hiển thị lịch sử lệnh

> ## **df**

Hiển thị báo cáo về việc sử dụng không gian đĩa của hệ thống

> ## **du**

Hiển thị chiếm bao nhiêu không gian trong mỗi tập tin. Điều này sẽ hiển thị kích thước trong số khối đĩa. Nếu bạn muốn xem nó theo byte, kilobyte và megabyte, hãy thêm `-h` đối số như thế này : `du -h`

> ## **ssh**

Đăng nhập từ xa vào một máy Linux khác, qua mạng.

Ví dụ: ssh vietanh@104.25.105.32 sẽ đăng nhập vào 104.25.105.32 bằng tên người dùng "vietanh"

