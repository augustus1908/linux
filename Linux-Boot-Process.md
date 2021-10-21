# Linux Boot Process

![alt](https://4.bp.blogspot.com/-srC-qTNDJd0/WQUXd670NNI/AAAAAAAAJFM/j6jj3_F0X5gtKy71s1QZK1I50MTF6GHhwCLcB/s320/linux-boot-process.png)

Có 6 giai đoạn của quá trình khởi động Linux

## 1.BIOS
* **Bios** - Basic Input/Output System - Hệ thống đầu ra/ đầu vào cơ bản
* Là bước đầu tiên của quá trình khởi, nó thực hiện công việc là *POST* (Power On Self Test)
* Đây là bài tự kiểm tra phần cứng, trạng thái thông số của nó ở 1 số vị trí như: CPU, bộ nhớ, card mạng, ...

## 2.MBR
* **MBR** (Master Boot Record) được lưu trữ tại sector đầu tiên của 1 thiết bị lưu dữ liệu 
* MBR chỉ 512byte = 1 sector 
* MBR chứa thông tin:
  * **Primary boot loader** (446 byte): cung cấp thông tin cho boot loader và vị trí boot loader trên ổ cứng.
  * **Partition table information** (64 byte): lưu trữ thông tin các partition
  * *Magic number* (2 byte): sử dụng để kiểm tra MBR, nếu MBR lỗi thì nó sẽ khôi phục lại.
 
## 3.GRUB
* Grand Unified Bootloader
* Sau khi xác định vị trí Boot Loader, bước này sẽ thực hiện load Boot Loader vào bộ nhớ và đọc thông tin cấu hình sau đó hiển thị GRUB Boot Menu để user lựa chọn.
* Nếu User không chọn OS thì sau khoảng thời gian định sẵn, GRUB sẽ load Kernel default vào memory để khởi động

## 4.Kernel
* **Kernel** của hệ điều hành sẽ được nạp vào trong RAM sau đó khi Kernel hoạt động thì việc đầu tiên sẽ thực thi quá trình INIT (SYSTEMD)

## 5.INIT
* Xem ở file ` /etc/initab` để xem Linux đang chạy ở level nào
* Các giai đoạn chính
  *  `0`: **halt**-Tắt hệ thống
  *  `1`: **single-user mod**-Không cấu hình network, khởi động các tiến trình và cho phép đăng nhập user non-root
  *  `2`: **multi-user mode**-không cấu hình network, khởi động các tiến trình.
  *  `3`: **multi-user mode with networking**-khởi động hệ thống bình thường trên giao diện dòng lệnh.
  *  `4`: **unused**
  *  `5`: **X11** - khởi động hệ thống trên giao diện đồ họa
  *  `6`: **reboot** - khởi động lại hệ thống.
 
## 6.Runlevel  
* Tùy thuộc vào cài đặt cấp init mặc định, hệ thống sẽ thực thi các chương trình từ một trong các thư mục sau
  * **Run level** `0`: /etc/rc.d/rc0.d/
  * **Run level** `1`: /etc/rc.d/rc1.d/
  * **Run level** `2`: /etc/rc.d/rc2.d/
  * **Run level** `3`: /etc/rc.d/rc3.d/
  * **Run level** `4`: /etc/rc.d/rc4.d/
  * **Run level** `5`: /etc/rc.d/rc5.d/
  * **Run level** `6`: /etc/rc.d/rc6.d/
