# Manage process

- **PID** Mỗi tiến trình có một định danh PID (Process Identify) duy nhất trong toàn bộ hệ thống vào thời điểm tiến trình đang chạy

- **PPID** Mỗi tiến trình đều có một tiến trình cha (parent process) với định danh là PPID (Parent process identify). Các tiến trình con (child process) thường được start bởi tiến trình cha (parent process). Một parents process có thể có nhiều child process nhưng một child process chỉ có một parents process

- **init** Init process là tiến trình đầu tiên được khởi động sau khi bạn lựa chọn hệ điều hành trong boot loader. Trong cây tiến trình, init process là tiến trình cha của các tiến trình khác

- **daemon** process là một tiến trình chạy nền (background). Các tiến trình này được bắt đầu khi khởi động hệ thống và sẽ tiếp tục được chạy mãi.

- **Zombie** thực chất là một phần còn sót lại của một tiến trình đã ngừng hoạt động nhưng chưa được xử lý sạch


## 1. ps
Process Status

Hiến thị thông tin liên quan đến tiến trình trong hệ thống : liệt kê các tiến trình hiện đang chạy và PID của nó và một số thông tin khác.

`[root@rhel7 ~]# ps

  PID TTY          TIME CMD
  
12330 pts/0    00:00:00 bash

21621 pts/0    00:00:00 ps
`

* PID - the unique process ID
* TTY - terminal type that user is logged into
* TIME - amount of CPU in minutes and seconds that the process has been running
* CMD - name of the command that launched the process

[option] 
* -e – Hiện tất cả processes.
* -f – Toàn bộ danh sách được format.
* -r – Chỉ hiện những process đang chạy.
* -u – chỉ định username (hoặc nhiều usernames).
* –p id – lọc dựa trên PID.
* –ppid – lọc dựa trên parent PID.
* -C – lọc dựa trên tên và command.
* -o – Hiện thông tin liên quan đến từ khóa cách nhau bởi khoảng trắng hoặc dấu phẩy

## 2. top
Hiến thị các tiến trình chạy real-time, hiển thị tóm tắt thông tin của hệ thống vá danh sách các quy trình hoặc luồng được quản lý bởi Kernel Linux

![](https://f7-zpcloud.zdn.vn/4049521945382909541/03667263dee711b948f6.jpg)

- **PID**: Shows task’s unique process id - id tiến trình
- **PR**: Stands for priority of the task - độ ưu tiên của tiến trình 
- **SHR**: Represents the amount of shared memory used by a task - dung lượng Ram share cho tiến trình
- **VIRT**: Total virtual memory used by the task - dung lượng Ram ảo thực hiện cho 1 tiến trình
- **USER**: User name of owner of task - người dùng sỡ hữu tiến trình 
- **%CPU**: Represents the CPU usage -  CPU sử dụng cho tiến trình
- **TIME+**: CPU Time, the same as ‘TIME’, but reflecting more granularity through hundredths of a second.
- **SHR**: Represents the Shared Memory size (kb) used by a task.
- **NI**: Represents a Nice Value of task. A Negative nice value implies higher priority, and positive Nice value means lower priority - giá trị nice value của tiến trình
- **%MEM**: Shows the Memory usage of task - bộ nhớ sử dụng cho tiến trình


- `k`	 Kills a process
- `M` 	Sorts the list by memory usage.
- `N` 	Sorts the list by PID.
- `r`	Changes the priority of a process.
- `h`	Displays the help window.
- `z`	Displays running processes in colors.
- `d`	Changes the refresh time interval.
- `c`	Displays the absolute path of a process.
- `CTRL+C` or `q`  Stops the top command.

## 3. htop
theo dõi tiến trình như `top` nhưng thao tác dễ dàng hơn

![](https://f7-zpcloud.zdn.vn/4175845875969019058/8ec82f9dcf1900475908.jpg)



## 4. FOREGROUND AND BACKGROUND PROCESS

- Foreground Process

  Theo mặc định , mọi process mà bạn bắt đầu chạy là foreground process . Nó nhận input từ bàn  phím và gửi output tới màn hình .

  Trong khi một chương trình đang chạy trong foreground và cần một khoảng thời gian dài, chúng ta không thể chạy bất kỳ lệnh khác (bắt đầu process khác) bởi vì dòng nhắc lệnh không có sẵn tới khi chương trình đang chạy kết thúc process và thoát ra.
  
- Background Process

  Background process chạy mà không được kết nối với bàn phím của bạn . Nếu backround process yêu cầu bất cứ đầu vào từ bàn phím , chương trinh sẽ đợi .

   Lợi thế của chạy một chương trình trong background là có thể chạy các lệnh khác : không phải đợi tới khi nó kết thúc để bắt đầu một process mới !














