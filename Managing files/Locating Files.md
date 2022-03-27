# Tools for Locating Files
## 1. `find`
used to find files and directories and perform subsequent operations on them. 

It supports searching by file, folder, name, creation date, modification date, owner and permissions

- **/ (slash)** — search the whole system.

- **. (dot)** — search from the folder you’re currently working on (current directory).

- ** ~ (tilde)** — to search from your home folder

------------------------------------------------

- `find [file/folder_name]`: tìm kiếm file/folder theo tên đầy đủ. 

- `find -name *`: tìm kiếm file theo tên không đầy đủ : `find . -name "*.txt" ; `find -name "index*"`

- `find / -perm 644`: tìm file có permission 644.


- Searching by Type

    d – directory or folder
    
    f – normal file
    
    l – symbolic link
    
    c – character devices
    
    b – block devices
    
  `find / -type f -name my-file`




## 2. `locate`

By default, Linux does not come with the locate command pre-installed.
```
sudo apt-get update
sudo apt-get install mlocate
```

Update the database :  `sudo updatedb`



- `locate [option] Pattern...`

- `locate *.txt`: Hiển thị file có đuôtxt

- `locate -i [file_name]`: phân biệt chữ hoa và chữ thường.
- `locate -c [file_name]`: trả về số lượng file
- `locate -e [file_name]`: Hiển thị các file tại thời điểm `locate` được chạy. 

## 3. `whereis`

- `whereis` chương trình giúp ta tìm :
   + Đường dẫn vị trí file binary.
   + Đường dẫn vị trí source code.
   + Đường dẫn vị trí manual dành cho chương trình hay lệnh đó.

- `whereis [options] program/command`

```
osboxes@osboxes:~$ whereis bash
bash: /bin/bash /etc/bash.bashrc /usr/share/man/man1/bash.1.gz
```
trong đó: 
- bash là tên lệnh.
- /bin/bash là đường dẫn đến file thực thi.
- /etc/bash.bashrc là file nguồn.
- /usr/share/man/man1/bash.1.gz là file man



- Các option
 + `-b`: tìm file binary 
 + `-m`: tìm file manual 
 + `-s`: tìm source code
 + `-B /path/dir`: tìm kiếm file binary ở thư mục được chỉ định.
 + `-M /path/dir`: tìm kiếm file manual ở thư mục được chỉ định.
 + `-S /path/dir`: tìm kiếm file source code ở thư mục được chỉ định.

## 4. `which`
Tìm ra đường dẫn các file chương trình nằm trong các directory liệt kê ở biến môi trường `$PATH`. 

```
osboxes@osboxes:~$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```
- which [-option][command]

```
osboxes@osboxes:~$ which cat
/bin/cat
osboxes@osboxes:~$ which ls gdb grep 
/bin/ls
/usr/bin/gdb
/bin/grep
```

## 5. So sánh `which` và `whereis`
- `whereis` liệt kê đường dẫn vị trí file binary, manual và source code còn `which` chỉ liệt kê đường dần file binary của chương trình lệnh.

```
osboxes@osboxes:~$ which cat
/bin/cat
osboxes@osboxes:~$ whereis cat
cat: /bin/cat /usr/share/man/man1/cat.1.gz
