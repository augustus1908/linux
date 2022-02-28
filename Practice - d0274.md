# Practice - 1

Thao tác trên Ubuntu Server 20.04

[Ubuntu Server Virtual Machine images for VMware and VirtualBox (osboxes.org)](https://www.osboxes.org/ubuntu-server/#ubuntu-server-20-04-2-vmware)

![Untitled](Practice%20-%20d0274/Untitled.png)

![Untitled](Practice%20-%20d0274/Untitled%201.png)

**Username:** osboxes

**Password:** osboxes.org

1. 1 số lưu ý khi thao tác lệnh

![Untitled](Practice%20-%20d0274/Untitled%202.png)

1. Thao tác lệnh cơ bản
    
    ![Untitled](Practice%20-%20d0274/Untitled%203.png)
    
    **`ls -l`**: hiện thị dưới dạng đầy đủ thông tin về file
    
    ![Untitled](Practice%20-%20d0274/Untitled%204.png)
    
    `ls -a` : hiển thị các file ẩn
    
    ![Untitled](Practice%20-%20d0274/Untitled%205.png)
    
    `echo $PATH`: hiển  giá trị của biến PATH
    
    ![Untitled](Practice%20-%20d0274/Untitled%206.png)
    
    ![Untitled](Practice%20-%20d0274/Untitled%207.png)
    
    `pwd` : cho biết mk đang ở đâu
    
    ![Untitled](Practice%20-%20d0274/Untitled%208.png)
    
    đổi tên dấu nhắc: 
    
    ![Untitled](Practice%20-%20d0274/Untitled%209.png)
    
    gõ `man ls` để tìm hiểu, cách sử dung về lệnh ls  
    
    gõ cách để sang trang
    
    gõ enter để xuống xem từ từ
    
    gõ q để quit   
    
    ![Untitled](Practice%20-%20d0274/Untitled%2010.png)
    
    hoặc gõ `man —help`
    
    dùng dấu `!!` để gọi lại câu lệnh vừa dùng   
    
    ![Untitled](Practice%20-%20d0274/Untitled%2011.png)
    
    dùng lệnh `cat` để hiển thị văn bản
    
    ![Untitled](Practice%20-%20d0274/Untitled%2012.png)
    
2. Đường dẫn
    
    ![Untitled](Practice%20-%20d0274/Untitled%2013.png)
    

1. Luyện tập
    1. Thay đổi mật khẩu
        
        ![Untitled](Practice%20-%20d0274/Untitled%2014.png)
        
        Sau đó gõ `exit` thoát ra và đăng nhập lại
        
    
    ***`Khi muốn thay đổi username (?)`***
    
    ![Untitled](Practice%20-%20d0274/Untitled%2015.png)
    
    b. Display the whole calendar for the year 2022
    
    gõ `cal 2022`
    
    ![Untitled](Practice%20-%20d0274/Untitled%2016.png)
    
    c. Bring up the man pages for the man command. Read the text that follows to obtain a better understanding of the functionality of the man command.
    
    Remember to use the space bar to go forward one screen and the return key to go forward one line. Press the b key to go back one screen. When you have read enough, exit man using the q key or <Ctrl c>.
    

1. Editing text file
    
    Gõ `vim <tên file>`
    
    Gõ `i` để vào chế độ INSERT, và có thể gõ được văn bản  
    
    ![Untitled](Practice%20-%20d0274/Untitled%2017.png)
    
    Nhấn esc để thoát → Gõ `:` sẽ chuyển đến last line mode, con trỏ sẽ ở dưới cùng, cho phép lưu hoặc thoát file   
    
    - Thoát + lưu file: Gõ `:wq!`
    - Thoát + ko lưu: Gõ `:q!`   hoặc `:x`
    
    Có thể lấy giá trị câu lệnh vừa chạy (mà ko cần thoát ra) vào file
    
    Ví dụ: gõ `:w!`  →   `:!ls -l`   →  `:r! ls`
    
    Cách di chuyển trong file
    
    ![Untitled](Practice%20-%20d0274/Untitled%2018.png)
    
    Các phím tắt nhanh
    
    ![Untitled](Practice%20-%20d0274/Untitled%2019.png)
    
    Các thao tác ở trong vim
    
    ![Untitled](Practice%20-%20d0274/Untitled%2020.png)