# Managing File Ownership

## chown
CHANGE OWNER
được dùng để thay đổi chủ sở hữu và nhóm sở hữu của file, thư mục, links nếu ta đang có quyển superuser của hệ thống Linux


chown [OPTION]… [OWNER][:[GROUP]] FILE…

chown [OPTION]… –reference=RFILE FILE…

chown owner_name file_name


![](https://f5-zpcloud.zdn.vn/8709318340764597112/72a000792dd1e28fbbc0.jpg)

OPTION:
- `*-c*` : báo cáo khi có sự thay đổi tập tin
- `*-v*` : hiển thị thông tin chi tiết
- `*-f*` : chặn thông báo lỗi


## chgrp
CHANGE GROUP OWNERSHIP 
Thay đổi quyền sở hữu nhóm của các tệp đã cho

chgrp [OPTION]… GROUP FILE…

chgrp [OPTION]… –reference=RFILE FILE…





























