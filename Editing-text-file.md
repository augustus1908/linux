# Editing text file
## 1. Vim

![](https://f5-zpcloud.zdn.vn/244505860166009097/9acd3e063ee7f1b9a8f6.jpg)

Khi ta vào vim, bắt đầu ở `normal` mode, ngoài ra còn có các modes `command, normal, visual, insert` 
Để chuyển từ `normal` sang `insert` ta ấn phím `i`
![](https://f6-zpcloud.zdn.vn/6395813378241601477/e1a876c53024ff7aa635.jpg)
Để lưu thay đổi và thoát ra, ta gõ `:wq`
![](https://f6-zpcloud.zdn.vn/3372666385101743784/ab6b81effa0e35506c1f.jpg)

* Các thao tác nhanh với vim
  * Di chuyển con trỏ trái, phải, xuống, lên với `H, I, J, K`
  * ![](https://f5-zpcloud.zdn.vn/6734083358683781907/5bf4c1bbb75a7804214b.jpg)
  * ![](https://f6-zpcloud.zdn.vn/2795200162416617138/b456491621f7eea9b7e6.jpg)
 
 
## 2. cat
cat [option] [file name]
Lệnh cat cho phép người dùng tạo một hoặc nhiều file, xem nội dung file, nối file và chuyển hướng đầu ra trong terminal hoặc file.
* Hiển thị nội dung: `# cat /etc/passwd`
* Hiển thị nội dung nhiều file: `# cat text text1`
* Tạo file: `# cat >text2`
* Xem nội dung file với tùy chọn more/less: `# cat vietanh.txt | more`
* Chuyển hướng file:
  * `cat text > text1` : text1 bị ghi đè bởi nội dung của file text
  * `cat text >> text1` : nội dung của text1 ghi xuống dười file 
 
* Các option của lệnh cat
  * -A : --show-all
  * -E : --show-ends : hiển thị $ ở cuối dòng và khoảng trống giữa các đoạn văn
  * -n : --number : hiển thị số dòng của file đó
  * -T : --show-tabs: hiển thị các dòng được phân tách bằng tab trong file, hiển thị thông qua ký tự ^I


## 3. split
split [option] [input [prefix]]
Lệnh `split` sử dụng để chia (hoặc tách) một tệp thành các phân đoạn có kích thước bằng nhau để xem và thao tác dễ dàng hơn và thường chỉ được sử dụng trên các tệp tương đối lớn. Theo mặc định, lệnh split tệp thành các phân đoạn 1000 dòng. Tệp gốc không thay đổi và một tập hợp các tệp mới có cùng tên cộng với tiền tố được thêm vào được tạo. Theo mặc định,tiền tố x được thêm vào
![](https://f6-zpcloud.zdn.vn/1064357205992230921/99d5d3dee03e2f60762f.jpg)

* Tách file dựa vào số dòng với option `-l` : `# split -l 4 index.txt split_file`
  ![](https://f5-zpcloud.zdn.vn/6626187084901925440/68d06f4737a7f8f9a1b6.jpg)

* Hiến thị chi tiết file tách với `--verbose`: `# split index.txt --verbose`

* Tách file theo size với `-b` : `# split -b index.txt index`
  ![](https://f5-zpcloud.zdn.vn/6719076830640647971/1be01027afc7609939d6.jpg)

* Tách file nhành n file nhỏ : `# split -n 3 index.txt`

## 4. sort
sort [option] [file name]
Lệnh sort được sử dụng để sắp xếp các dòng của tệp văn bản theo thứ tự tăng dần hoặc giảm dần, theo một khoá sắp xếp. Khóa sắp xếp mặc định là thứ tự của các ký tự ASCII (theo thứ tự bảng chữ cái).

* option `-o` - output to a new file:
  ![](https://f6-zpcloud.zdn.vn/5556538597578206951/2835c58f226fed31b47e.jpg)

* option `-r` - sorting in reverse order: sắp xếp ngược lại
  ![](https://f6-zpcloud.zdn.vn/3259948770550786173/2395d8d5c93606685f27.jpg)

* option `-n` - numerically : sắp xếp số tăng dần : `sort -n index.txt`
* option `-nr` : sắp xếp số giảm dần : `sort -nr index.txt`
* option `-k` : sắp xếp dữ liệu của 1 cột
* option `-c` : kiểm tra xem file đã bị sắp xếp hay chưa, nếu không hiện output thì file được coi là đã sắp xếp rồi 
* option `-u`: sắp xếp và loại đi các phần tử giống nhau
* option `-M` : sort by month


## 5. uniq
uniq [option] [input[output]]
`uniq` dùng để bỏ các dòng liên tiếp trùng lặp trong một tệp văn bản rất hữu ích để đơn giản hóa hiển thị văn bản.
![](https://f5-zpcloud.zdn.vn/3462309147255511007/78d1abedcf0e0050591f.jpg)

* option `-c` : cho biết số dòng bị lặp lại
  ![](https://f6-zpcloud.zdn.vn/8981235003454679815/9ba8ab4e3badf4f3adbc.jpg)

* option `-d` : chỉ hiện những dòng bị lặp lại
* option `-u` : chỉ in những dòng duy nhất (không lặp lại)





