**File system** được dùng để quản lý cách dữ liệu được đọc và lưu trên thiết bị.

![](https://f7-zpcloud.zdn.vn/6048275269572346221/cc7bbf91e5122a4c7303.jpg)


## Các loại filesystem
- Các lại cơ bản: EXT2, EXT3, XFS, JFS
- Dành cho dạng lưu trữ Flash: thẻ nhớ
- Dành cho hệ cơ sở dữ liệu
- Dành cho mục đích khác


## Phân vùng
Một phân vùng là một vùng chứa trong đó có một filesystem được lưu trữ , trong một số trường hợp thì filesystem có thể mở rộng hơn một phân vùng nếu filesystem sử dụng các liên kết.

## Filesystem Hierarchy Standard (FHS)

FHS là tiêu chuẩn cấp bậc của hệ thống tập tin filesystem trên hệ điều hành Linux. Việc có một tiêu chuẩn thế này hữu ích cho người dùng, quản trị viên, lập trình viên có thể chuyển đổi giữa các distro

![](https://f5-zpcloud.zdn.vn/9075325721465440655/3270fe10c98006de5f91.jpg)


Linux dùng ký tự “/” để tách các đường dẫn (khác với Windows sử dụng “\” để tách các đường dẫn). Tất cả các tập tin thư mục đều được bắt đầu từ thư mục gốc (/), cũng không có ký tự ổ đĩa giống Windows.

Chức năng của các thư mục:

**/bin**: Các chương trình cơ bản

**/boot**: chứa nhân Linux (kernel Linux) để khởi động và các filesystem maps cũng như các file khởi động giai đoạn 2.

**/dev**: chứa các tập tin thiết bị (CDRom, HDD, FDD,…)

**/etc**: chứa các tập tin cấu hình hệ thống.

**/home**: thư mục dành cho người dùng không phải là root

**/lib**: chứa các thư viện dùng chung cho các lệnh nằm trong /bin và /sbin. Thư mục này cũng chứa các module của kernel.

 
**/mnt** hoặc **/media**: mount point mặc định cho những hệ thống file kết nối bên ngoài.

**/opt**: thư mục chứa các phần mềm cài thêm

**/sbin**: các chương trình hệ thống

**/srv**: dữ liệu được sử dụng bởi các máy chủ lưu trữ trên hệ thống

**/tmp**: thư mục chứa các file tạm thời, xóa đi khi reboot hoặc shutdown

**/usr**: thư mục chứa những file cố định hoặc quan trọng để phục vụ tất cả người dùng

**/var**: dữ liệu biến được xử lý bởi daemon, điều này bao gồm các tệp nhật ký, hàng đợi,
cache,…

**/root**: các tệp cá nhân của người quản trị (root account)

**/proc**: sử dụng cho nhân Linux, chúng được sử dụng bởi kernel để xuất dữ liệu sang không gian người dùng.


## File System Consistency Checker (FSCK)

fsck (kiểm tra hệ thống tệp) là một tiện ích dòng lệnh cho phép bạn thực hiện kiểm tra tính nhất quán và sửa chữa tương tác trên một hoặc nhiều hệ thống tệp Linux. Nó sử dụng các chương trình dành riêng cho loại hệ thống tập tin mà nó kiểm tra.
có thể sử dụng lệnh fsck để sửa chữa các hệ thống tệp bị hỏng trong trường hợp hệ thống không khởi động được hoặc không thể gắn phân vùng.


fsck [option] [file]

-A: Áp dụng để kiểm tra tất cả các hệ thống tập tin. 

-C: Hiển thị thanh tiến trình.

-l: Khóa thiết bị để đảm bảo rằng không có chương trình nào khác sẽ cố gắng sử dụng phân vùng trong khi xác minh và do đó gây ra lỗi

-M: Không xác minh hệ thống tập tin gắn kết.

-N: triển khai hành động được thực hiện nhưng không thực sự thực hiện nó.

-P: Cho phép bạn kiểm tra các hệ thống tệp song song, bao gồm cả root.

-R: Không kiểm tra hệ thống tập tin gốc. Điều này chỉ hữu ích với '-A'.

-r: cung cấp số liệu thống kê cho từng thiết bị đang được kiểm tra.

-T: Không hiển thị tiêu đề.

-t: Nó cho phép chúng tôi chỉ định độc quyền các loại hệ thống tệp để xác minh. Các loại có thể là một danh sách được phân tách bằng dấu phẩy.

-V: Cung cấp mô tả về hành động được thực hiện.



































