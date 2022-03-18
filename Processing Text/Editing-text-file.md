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


## 3. sort
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


## 4. uniq
uniq [option] [input[output]]

`uniq` dùng để bỏ các dòng liên tiếp trùng lặp trong một tệp văn bản rất hữu ích để đơn giản hóa hiển thị văn bản.
![](https://f5-zpcloud.zdn.vn/3462309147255511007/78d1abedcf0e0050591f.jpg)

* option `-c` : cho biết số dòng bị lặp lại
  ![](https://f6-zpcloud.zdn.vn/8981235003454679815/9ba8ab4e3badf4f3adbc.jpg)

* option `-d` : chỉ hiện những dòng bị lặp lại
* option `-u` : chỉ in những dòng duy nhất (không lặp lại)


## 5. paste
paste [option] ... [files] .... 

Lệnh paste được sử dụng để kết hợp các trường từ các tệp khác nhau, cũng như kết hợp các dòng từ nhiều tệp.

Ví dụ: Dòng một từ file1 có thể được kết hợp với dòng một của file2 , dòng hai từ file1 có thể được kết hợp với dòng hai của file2,...

![](https://f6-zpcloud.zdn.vn/233656039678300123/6c0c8f4159a396fdcfb2.jpg)

* option `-d` : delimiter : lệnh `paste` mặc định dùng dấu tab phân cách khi sáp nhập file. có thể thay đổi ký tự phân cách bằng cách sử dụng `-d` . nếu nhiều hơn 1 ký tự thì `paste` sẽ sử dụng lần lượt ký tự phân cách theo hình thức vòng tròn.
  ![](https://f5-zpcloud.zdn.vn/5991077363715441595/72b5868d756fba31e37e.jpg)

* option `-s` : serial : Nối dữ liệu theo chuỗi chứ không phải song song. Theo chiều ngang chứ không phải theo chiều dọc.
  ![](https://f5-zpcloud.zdn.vn/7831400575937355467/7e926d2a80c84f9616d9.jpg)


## 6. join
join [option] file1 file2

`join` nâng cao của `paste` , khi các tệp có 1 trường **key** chung, `join` sẽ kết hợp các tệp lại dựa vào trường chung đó

![](https://f6-zpcloud.zdn.vn/6608635358684525220/130b37be3853f70dae42.jpg)

* option `-a FILENUM` : ghép 2 tệp khi trường chung không cùng số lượng với nhau
 ![](https://f6-zpcloud.zdn.vn/5293913130588066429/32f24bfd0410cb4e9201.jpg)
 
* option `v FILENUM` : hiển thị dòng không giao nhau của trường chung giữa các tệp
 ![](https://f6-zpcloud.zdn.vn/2294660110992017072/ef7baeded1331e6d4722.jpg)

* sử dụng -1, -2 và option `-j[field]` : -1 -2 lần lượt là tệp thứ 1, tệp thứ 2, đi kèm sau là trường chung ở cột nào của tệp tương ứng đấy; nếu 2 tệp có trường chung ở chung 1 cột (ví dụ trường chung ở cùng cột 2) thì dùng `$ join -j2 text1 text2 `
 ![](https://f6-zpcloud.zdn.vn/8341454788910827089/e431100ab2e77db924f6.jpg)
 
* option `-i` : ignore : nếu trường chung 1 tệp là chữ in thường, 1 tệp chữ in hoa thì sử dụng `-i`
* option `--nocheck-order` : để loại bỏ việc báo lỗi/ cảnh báo khi `join` kiểm tra đầu vào đã sắp xếp hay chưa 
* option `-t` : sử dụng để chỉ định dấu phân cách khi gộp file :`$join -t, file1.txt file2.txt`


## 7. split
split [option] [input [prefix]]

Lệnh `split` sử dụng để chia (hoặc tách) một tệp thành các phân đoạn có kích thước bằng nhau để xem và thao tác dễ dàng hơn và thường chỉ được sử dụng trên các tệp tương đối lớn. Theo mặc định, lệnh split tệp thành các phân đoạn 1000 dòng. Tệp gốc không thay đổi và một tập hợp các tệp mới có cùng tên cộng với tiền tố được thêm vào được tạo. Theo mặc định,tiền tố x được thêm vào
![](https://f6-zpcloud.zdn.vn/1064357205992230921/99d5d3dee03e2f60762f.jpg)

* Tách file dựa vào số dòng với option `-l` : `# split -l 4 index.txt split_file`
  ![](https://f5-zpcloud.zdn.vn/6626187084901925440/68d06f4737a7f8f9a1b6.jpg)

* Hiến thị chi tiết file tách với `--verbose`: `# split index.txt --verbose`

* Tách file theo size với `-b` : `# split -b index.txt index`
  ![](https://f5-zpcloud.zdn.vn/6719076830640647971/1be01027afc7609939d6.jpg)

* Tách file nhành n file nhỏ : `# split -n 3 index.txt`


## 8. nl
nl [option].... [file]....
đánh số dòng trong tệp

![](https://f7-zpcloud.zdn.vn/5127238521300425304/cd0000192ef5e1abb8e4.jpg)

* option `-b number` : numbering body lines
* option `-i number` : line number increment at each line
* option `-n format` : insert line numbers according to FORMAT
* option `-v number` : change first line number of the given input
* option `-s string` : add any STRING after every logical line number
* option `-l number` : group of NUMBER empty lines are counted as one














