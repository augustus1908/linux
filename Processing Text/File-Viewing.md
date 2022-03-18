# File Viewing

## 1. Head
head [option]...[file]...

In ra phần đầu của tệp, mặc định là 10 dòng đầu

* option `-n number` --lines : in số dòng muốn hiện ra : `$head -n 5 index.txt` (in ra 5 dòng đầu tiên)
* option `-c number` --bytes : in ra số bytes đầu tiên của tệp : `$head -c 6 index.txt`
* option `-q` --quiet : khi dùng `head` đồng thời với nhiều tệp, sử dụng `-q` bỏ đi tên tệp trước mỗi head được trích ra 
![](https://f6-zpcloud.zdn.vn/6431062013823147857/2ca832998c75432b1a64.jpg)

* option `-v` --verbose : hiện tên tệp khi head trích ra 


## 2. Tail
tail [option]... [file]...

In ra phần cuối của tệp, mặc định là 10 dòng cuối

* option `-n num` : `$tail -n 3 index.txt` or `$tail -3 index.txt` 

  `$tail +25 index.txt` : in từ dòng 25 đến cuối của tệp
  
* option `-c num` 
* option `-q`
* option `-v`
* option `-f` : giám sát, xem nhật ký tệp; cho xem 10 dòng cuối của tệp và cập nhật những dòng lệnh mới 



