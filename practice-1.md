Thao tác trên Ubuntu Server 20.04

[Ubuntu Server Virtual Machine images for VMware and VirtualBox (osboxes.org)](https://www.osboxes.org/ubuntu-server/#ubuntu-server-20-04-2-vmware)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/199c5ee9-255c-4156-8986-f706e822e847/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0c0e151e-7829-45e7-aa78-0aa4ff6bccf3/Untitled.png)

**Username:** osboxes

**Password:** osboxes.org

1. 1 số lưu ý khi thao tác lệnh

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5f7be369-f698-4097-b5f3-b3fc621fc6a7/Untitled.png)

1. Thao tác lệnh cơ bản
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e4f45441-d77e-482c-947f-dfb9427b9fc7/Untitled.png)
    
    **`ls -l`**: hiện thị dưới dạng đầy đủ thông tin về file
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a730c9a3-388d-43b4-8818-5e9dba2f6031/Untitled.png)
    
    `ls -a` : hiển thị các file ẩn
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f2a2c30-d388-44b2-9b2f-0ebf40fa439f/Untitled.png)
    
    `echo $PATH`: hiển  giá trị của biến PATH
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f813c1fd-6556-4c4c-abc0-bb87c4c55e3f/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/95ad04b2-0cf3-4a95-843b-78bbe41e30a7/Untitled.png)
    
    `pwd` : cho biết mk đang ở đâu
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/85f7737e-258e-4b41-b3c6-2b044283b690/Untitled.png)
    
    đổi tên dấu nhắc: 
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78e73913-11b5-48e6-b39c-18e068f8938a/Untitled.png)
    
    gõ `man ls` để tìm hiểu, cách sử dung về lệnh ls  
    
    gõ cách để sang trang
    
    gõ enter để xuống xem từ từ
    
    gõ q để quit   
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3d8a39a2-a27a-4e6a-a587-329fd426618c/Untitled.png)
    
    hoặc gõ `man —help`
    
    dùng dấu `!!` để gọi lại câu lệnh vừa dùng   
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/877e5669-9707-4ff2-8180-6c8edfa77a7c/Untitled.png)
    
    dùng lệnh `cat` để hiển thị văn bản
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22db1f33-213e-44dd-9325-f56f6837a22e/Untitled.png)
    
2. Đường dẫn
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0e84d604-a481-4cf5-9920-807e764c08ca/Untitled.png)
    

1. Luyện tập
    1. Thay đổi mật khẩu
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61ef307e-7005-4ee6-a96d-ebb7ed2fa026/Untitled.png)
        
        Sau đó gõ `exit` thoát ra và đăng nhập lại
        
    
    ***`Khi muốn thay đổi username (?)`***
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de930fc6-dd8c-495b-ac69-d4ebe762a24e/Untitled.png)
    
    b. Display the whole calendar for the year 2022
    
    gõ `cal 2022`
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ced1b9ac-0a52-4262-9de7-9bf0c847fae4/Untitled.png)
    
    c. Bring up the man pages for the man command. Read the text that follows to obtain a better understanding of the functionality of the man command.
    
    Remember to use the space bar to go forward one screen and the return key to go forward one line. Press the b key to go back one screen. When you have read enough, exit man using the q key or <Ctrl c>.
    

1. Editing text file
    
    Gõ `vim <tên file>`
    
    Gõ `i` để vào chế độ INSERT, và có thể gõ được văn bản  
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b8159d2b-f2d9-426f-940a-a991a736c0dc/Untitled.png)
    
    Nhấn esc để thoát → Gõ `:` sẽ chuyển đến last line mode, con trỏ sẽ ở dưới cùng, cho phép lưu hoặc thoát file   
    
    - Thoát + lưu file: Gõ `:wq!`
    - Thoát + ko lưu: Gõ `:q!`   hoặc `:x`
    
    Có thể lấy giá trị câu lệnh vừa chạy (mà ko cần thoát ra) vào file
    
    Ví dụ: gõ `:w!`  →   `:!ls -l`   →  `:r! ls`
    
    Cách di chuyển trong file
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/737e3fdc-eed6-4337-99e0-e157edd9ec72/Untitled.png)
    
    Các phím tắt nhanh
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/880ac45c-492e-411e-aa08-232dca0f3088/Untitled.png)
    
    Các thao tác ở trong vim
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d06fa0df-1510-4e88-b6ab-00be43a2325f/Untitled.png)
