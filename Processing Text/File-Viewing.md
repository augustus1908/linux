# File Viewing

## 1. Head
head [option]...[file]...

In ra phần đầu của tệp, mặc định là 10 dòng đầu

* option `-n number` --lines : in số dòng n đầu tiên của tệp : `$head -n 5 index.txt` (in ra 5 dòng đầu tiên)
* option `-c number` --bytes : in ra số bytes đầu tiên của tệp : `$head -c 6 index.txt`
* option `-q` --quiet : không in tiêu đề xác định tên tệp 
![](https://f6-zpcloud.zdn.vn/6431062013823147857/2ca832998c75432b1a64.jpg)

* option `-v` --verbose : luôn in tiêu đề xác định tên tệp 


## 2. Tail
tail [option]... [file]...

In ra phần cuối của tệp, mặc định là 10 dòng cuối

* option `-n num` : `$tail -n 3 index.txt` or `$tail -3 index.txt` 

  `$tail +25 index.txt` : in từ dòng 25 đến cuối của tệp
  
* option `-c num` 
* option `-q`
* option `-v`
* option `-f` : giám sát, xem nhật ký tệp; cho xem 10 dòng cuối của tệp và cập nhật những dòng lệnh mới 


## 3. less
less [option] [file]

Dùng để đọc nội dung 1 trang của 1 tệp tại 1 thời điểm. Khả năng tải nhanh hơn đối với các tệp lớn vì nó chỉ tải 1 phần của tệp

* `Space` hoặc `f` : di chuyển xuống trang mới
* `b` : di chuyển lên lại trang phía trên (có thể dùng mũi tên để di chuyển)
* `G ` : di chuyển đến cuối tập tin
* `g ` : di chuyển đến đầu tập tin
* `q` : thoát tệp hiện tại
* tìm kiếm một chuỗi : `/{chuỗi}` hoặc `?{chuỗi}`

* option `-N` : hiển thị số dòng 
* option `-X` : giữ nội dung khi thoát tệp
* option `+F` : mở nhật ký tệp ~ `tail -f`


## 4. cut
cut [OPTION] ... [FILE] ...

`cut` là một tiện ích dòng lệnh cho phép bạn cắt các phần của dòng từ các tệp hoặc dữ liệu được chỉ định và in kết quả ra đầu ra tiêu chuẩn. Nó có thể được sử dụng để cắt các phần của một dòng theo dấu phân cách, vị trí byte và ký tự.

* option `-b` (--bytes=LIST) : trích xuất theo bytes : `$ cut -b 1,2,3 state.txt` ; `$ cut -b -3 state.txt`
* option `-f` (--fields) : trích xuất bằng cách chỉ định một trường, một tập hợp các trường hoặc một phạm vi trường. Đây là tùy chọn được sử dụng phổ biến nhất : `$ cut -f 1 state.txt` ; `$cut -d "delimiter" -f (field number) file.txt`
* option `-d` ( --delimiter) : Chỉ định một dấu phân cách sẽ được sử dụng thay cho dấu phân cách “TAB” mặc định.
* option `-c` (--characters) : trích xuất bằng cách chỉ định 1 ký tự, một bộ ký tự hoặc một dải ký tự : `$ cut -c 2,5,7 state.txt` (lấy các ký tự ở vị trí 2,5,7) ; `$ cut -c 1-7 state.txt` ;...
* 
  

















