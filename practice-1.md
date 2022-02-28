Thao tác trên Ubuntu Server 20.04

[Ubuntu Server Virtual Machine images for VMware and VirtualBox (osboxes.org)](https://www.osboxes.org/ubuntu-server/#ubuntu-server-20-04-2-vmware)

![Untitled](https://f6-zpcloud.zdn.vn/5138868467967139719/86341b6edadb16854fca.jpg)

![Untitled](https://f6-zpcloud.zdn.vn/9166419512134421431/9d36a56c64d9a887f1c8.jpg)

**Username:** osboxes

**Password:** osboxes.org

1. 1 số lưu ý khi thao tác lệnh

![Untitled](https://f4-zpcloud.zdn.vn/4694588742197033257/8da8e78d2638ea66b329.jpg)

2. Thao tác lệnh cơ bản


    
    ![Untitled](https://f5-zpcloud.zdn.vn/423317260679165136/5bc834eef55b3905604a.jpg)
    
    
    `ls -l`: hiện thị dưới dạng đầy đủ thông tin về file
    
    ![Untitled](https://f6-zpcloud.zdn.vn/647546522591674623/ccb67196b0237c7d2532.jpg)
    
    
    `ls -a` : hiển thị các file ẩn
    
    ![Untitled](https://f5-zpcloud.zdn.vn/8249730688907762210/4118633aa28f6ed1379e.jpg)
    
    
    `echo $PATH`: hiển  giá trị của biến PATH
    
    ![Untitled](https://f5-zpcloud.zdn.vn/7878888975537231730/5c9c9bae5a1b9645cf0a.jpg)
    
    
    
    `pwd` : cho biết mk đang ở đâu
    
    ![Untitled](https://f5-zpcloud.zdn.vn/8390800314785856442/9a2535c6fb73372d6e62.jpg)
    
    đổi tên dấu nhắc: 
    
    ![Untitled](https://f5-zpcloud.zdn.vn/2348999363693395066/4b46dcaa121fde41870e.jpg)
    
    gõ `man ls` để tìm hiểu, cách sử dung về lệnh ls  
    
    gõ cách để sang trang
    
    gõ enter để xuống xem từ từ
    
    gõ q để quit   
    
    ![alt](https://f4-zpcloud.zdn.vn/5395890411486226097/96c7d929179cdbc2828d.jpg)
    
    hoặc gõ `man —help`
    
    dùng dấu `!!` để gọi lại câu lệnh vừa dùng   
    
    ![Untitled](https://f6-zpcloud.zdn.vn/3093646698729140492/d29fe5772bc2e79cbed3.jpg)
    
    dùng lệnh `cat` để hiển thị văn bản
    
    ![Untitled](https://f6-zpcloud.zdn.vn/1132488600684826233/ffc82222ec9720c97986.jpg)
    
3. Đường dẫn
    
    ![Untitled](https://f4-zpcloud.zdn.vn/1533671290698418183/d9efd3051db0d1ee88a1.jpg)
    

4. Luyện tập


    a. Thay đổi mật khẩu
    
        
        ![](https://f4-zpcloud.zdn.vn/3972179308426930096/e01123e5ed50210e7841.jpg)
        
        
        Sau đó gõ `exit` thoát ra và đăng nhập lại
        
    
    b. Display the whole calendar for the year 2022
    
    gõ `cal 2022`
    
    ![Untitled](https://f6-zpcloud.zdn.vn/8031577525588441331/d0995a6e94db588501ca.jpg)
    
    c. Bring up the man pages for the man command. Read the text that follows to obtain a better understanding of the functionality of the man command.
    
    Remember to use the space bar to go forward one screen and the return key to go forward one line. Press the b key to go back one screen. When you have read enough, exit man using the q key or <Ctrl c>.
    


5. Editing text file
    
    Gõ `vim <tên file>`
    
    Gõ `i` để vào chế độ INSERT, và có thể gõ được văn bản  
    
    Nhấn esc để thoát → Gõ `:` sẽ chuyển đến last line mode, con trỏ sẽ ở dưới cùng, cho phép lưu hoặc thoát file   
    
    - Thoát + lưu file: Gõ `:wq!`
    - Thoát + ko lưu: Gõ `:q!`   hoặc `:x`
    
    Có thể lấy giá trị câu lệnh vừa chạy (mà ko cần thoát ra) vào file
    
    Ví dụ: gõ `:w!`  →   `:!ls -l`   →  `:r! ls`
    
    Cách di chuyển trong file
    
    ![Untitled](https://f6-zpcloud.zdn.vn/8249011349291677571/f6967160bfd5738b2ac4.jpg)
    
    Các phím tắt nhanh
    
    ![Untitled](https://f6-zpcloud.zdn.vn/604193329080215412/c8e28a1544a088fed1b1.jpg)
    
    Các thao tác ở trong vim
    
    ![Untitled](https://f4-zpcloud.zdn.vn/194048750471199828/e83724c1ea74262a7f65.jpg)
