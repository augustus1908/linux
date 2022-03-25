# Controlling Access to Files

- 3 quyền hạn cơ bản của 1 user/group trên file/folder bao gồm:
   - r (read)- Quyền đọc file. (4)
   - w (write)- Quyền ghi, sửa nội dung file. (2)
   - x (execute)-Quyền thực thi(truy cập) thư mục. (1)

![](https://f6-zpcloud.zdn.vn/4525762847009581565/2849159cce34016a5825.jpg)

- rw-: đối tượng thứ nhất là quyền user sở hữu nó.
- rw-: đối tượng thứ 2 là quyền cho các user thuộc group sở hữu nó.
- r--: đối tượng thứ 3 là quyền dành cho mọi user không.


## chmod
CHANGE MODE

chmod [option] [Phân quyền] [file/folder_name]

- Xác định người dùng nào được quyền cho tệp được thay đổi
    **u** – user - Chủ sở hữu hồ sơ.
    
    **g** – group - Người dùng là thành viên của nhóm.
    
    **o** – other - Tất cả những người dùng khác.
    
    **a** – all - Tất cả người dùng, giống ugo

- Xác định xem các quyền có được gỡ bỏ, thêm hoặc đặt hay đặt:
   ` - ` Loại bỏ các quyền đã chỉ định.
   
    ` + ` Thêm các quyền được chỉ định.
    
    ` = ` Thay đổi các quyền hiện tại đối với các quyền đã chỉ định. Nếu không có quyền nào được chỉ định sau ký hiệu =, tất cả các quyền từ lớp người dùng được chỉ định sẽ bị xóa.

- Mỗi quyền ghi, đọc và thực thi có giá trị số sau:
      r (đọc) = 4
      
      w (viết) = 2
      
      x (thực hiện) = 1
      
      không có quyền = 0
      
Ví dụ : `chmod ugo-rwx xyz.txt` - hủy bỏ quyển đọc, viết, thực thi đối với toàn bộ người dùng, nhóm, người dùng khác khỏi tệp xyz.txt



# Managing File Ownership

## chown
CHANGE OWNER

được dùng để thay đổi chủ sở hữu và nhóm sở hữu của file, thư mục, links nếu ta đang có quyển superuser của hệ thống Linux


chown [OPTION]… [OWNER][:[GROUP]] FILE…

chown [OPTION]… –reference=RFILE FILE…

chown owner_name file_name


![](https://f5-zpcloud.zdn.vn/8709318340764597112/72a000792dd1e28fbbc0.jpg)

OPTION:
- `**-c**` : báo cáo khi có sự thay đổi tập tin
- `**-v**` : hiển thị thông tin chi tiết
- `**-f**` : chặn thông báo lỗi


## chgrp
CHANGE GROUP OWNERSHIP 

Thay đổi quyền sở hữu nhóm của các tệp đã cho

chgrp [OPTION]… GROUP FILE…

chgrp [OPTION]… –reference=RFILE FILE…





























