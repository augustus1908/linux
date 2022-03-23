## File System Consistency Checker (FSCK)

fsck (kiểm tra hệ thống tệp) là một tiện ích dòng lệnh cho phép bạn thực hiện kiểm tra tính nhất quán và sửa chữa tương tác trên một hoặc nhiều hệ thống tệp Linux. Nó sử dụng các chương trình dành riêng cho loại hệ thống tập tin mà nó kiểm tra.
có thể sử dụng lệnh fsck để sửa chữa các hệ thống tệp bị hỏng trong trường hợp hệ thống không khởi động được hoặc không thể gắn phân vùng.


fsck [option] [partition]

-A: Duyệt khắp và kiểm tra tất cả các hệ thống tập tin trong 1 lần duyệt.

-V: chế độ chi tiết, cho biết fsck đang làm gì

-t: xác định hệ thống tập tin cần kiểm tra

-a: Tự động sửa chữa hệ thống tập tin.

-l: Liệt kê tất cả các tên tập tin trong hệ thống tập tin

-r: hỏi trước khi sửa chữa hệ thống tập tin



## Monitoring Disk

### 1. df
DISK FILESYSTEM

df [option] ... [file] ...

Được dùng để lấy toàn bộ thông tin về lượng ổ cứng khả dụng và lượng ổ cứng đã dùng bởi các phân vùng (partition).

![](https://f6-zpcloud.zdn.vn/4056597831803378453/45477b49eeda218478cb.jpg)

- **filesystem**: tên filesystem có thể trùng với phân vùng đĩa.
- **1K-blocks**: Số lượng khối (block) có trong filesystem có kích thước 1Kb.
- **Used**: Số lượng 1K-block được sử dụng trong filesystem.
- **Available**: Số lượng 1K-block đang có sẵn.
- **Use%**: Phần trăm đĩa đã sử dụng trong filesystem.
- **Mounted on**: Nơi mount.

option:

- `-h` : Hiển thị thông tin ổ đĩa theo định dạng dễ đọc
![](https://f6-zpcloud.zdn.vn/8730875925442365976/6990cb147787b8d9e196.jpg)


- `-a` : hiện thị toàn bộ thông tin về file hệ thống
- `-T` : xem loại file
- `-i` hoặc `--inodes` : kiểm tra inode đã sử dụng


### 2. du
DISK USAGE

du [option] [path|file]

du [option] [path1] [path2] [path3]

Hiển  dung lượng ổ đĩa được sử dụng bởi các thư mục (directory) và file

Đơn vị mặc định là bytes


## Creating Filesystems
MAKE FILE SYSTEM

mkfs <option> Devicename (partition)
  
`-t`: Chỉ định type cho hệ thống. Nếu không chỉ định type thì mặc định là ext2.
  
`-c`: trước khi tạo file hệ thống thì tiến hành check bad block.
  
Định dạng cho partition bằng command: `mkfs.ext4 <new_partition>`


## Mounting and Unmounting Filesystems
**mount** đề cập đến một quá trình cho phép máy tính truy cập các file trên nhiều thiết bị khác nhau, chẳng hạn như USB hoặc ổ cứng. Điều này là do chúng bắt nguồn từ các hệ thống file riêng biệt. 

Toàn bộ mount trong hệ thống lưu trong /etc/fstab
  ![](https://f6-zpcloud.zdn.vn/656976804553489976/912bb9991104de5a8715.jpg)

`mount -f fstype device mountpoint`

l : Lists all the file systems mounted yet.
h : Displays options for command.
V : Displays the version information.
a : Mounts all devices described at /etc/fstab.
t : Type of filesystem device uses.
T : Describes an alternative fstab file.
r : Read-only mode mounted.

## Partition Disks
Một partition là sự tách biệt logical ra khỏi toàn bộ ổ đĩa. Nhưng nó xuất hiện như thể sự phân chia tạo ra nhiều ổ đĩa vật lý.

Các điều kiện được liên kết với một partition bao gồm các partition chính (primary), hoạt động (active), mở rộng (extend) và logic.

Việc chia một ổ đĩa cứng thành các partition rất hữu ích vì nhiều lý do nhưng lý do chính là để cung cấp ổ đĩa có sẵn cho một hệ điều hành

### fdisk
FORMAT DISK
  
Nó được sử dụng để xem, tạo, xóa, thay đổi, thay đổi kích thước, sao chép và di chuyển các phân vùng trên ổ cứng bằng giao diện điều khiển hộp thoại.
 
Cho phép tạo ra tối đa 4 phân vùng primary, còn phân vùng logic phụ thuộc vào kích thước của đĩa cứng mà ta sử dụng

`fdisk [option] device `

- `sudo fdisk -l` : xem toàn bộ phân vùng ổ đĩa
 
- `sudo fdisk -l /dev/sda` : xem toàn bộ phân vùng ổ đĩa trên thiết bị /dev/sda
  
- `sudo fdisk -s /dev/sda` : xem kích thước của phân vùng
  

Ấn m để thấy hết các tùy chọn
Ấn n để tạo phân vùng mới
Ấn d để xóa phân vùng khỏi ổ đĩa và giải phóng dung lượng
![](https://f5-zpcloud.zdn.vn/419097643625438136/4392c3aa963659680027.jpg)
  








































