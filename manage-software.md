# Manager software

## Packages
+ Package files: đơn vị cơ bản nhất của 1 package, là một dạng file chứa tất cả thông tin cần thiết để cài đặt chương trình  
+ Repository: Nơi tập chung chứa các package file, một distribution có thể có vài repo với các mục đích khác nhauMột nơi tập trung chứa các package files, một distribution có thể có một vài repositories khác nhau phục vụ nhiều mục đích khác nhau, hoặc phục vụ cho từng quá trình phát trình phần mềm (repository cho quá trình test,...).
+ Dependencies: Một package thì rất it khi mang tính standalone mà nó thường được xây dựng dựa trên các package khác, cũng giống như khi các bạn lập trình, khi cài đặt sử dụng một thư viện thì thư viện đó đều xây dựng dựa trên một thư viện khác, các thư viện khác đó gọi là dependencies.
+ 2 loại package system phổ biến : Debian (.deb) và Red Hat (.rpm)
+ Binary package: Các gói được chuẩn bị trên hệ thống để cài đặt dễ dàng hơn

**Tool**
+ Low-level package tool: chịu trách nhiệm cho các tác vụ như install, remove : dkpg, rpm 
+ High-level package tool: xử lí tác vụ liên quan tìm kiếm thông tin và cài đặt dependencies : apt, zypper, yum

  
 ## Tar
 Tape archive, là một lệnh phổ biến nhất để nén và giải nén file và thư mục trong Linux
 
 - **c** : tạo file .tar mới
 - **v** : hiển thị quá trình nén lên màn hình
 - **f** : chỉ đến file lưu trữ sẽ tạo
 - **z** : nén với gzip (nén mạnh hơn tar) 
 - **j** : nén với bunzip 2 (nén nhiều hơn gzip)
 - **x** : giải nén file
 - **C** : giải nén file sang thư mục khác
 
 Tạo file nén : `tar -cvf sampleArchive.tar /home/sampleArchive` ...
 Giải nén : `tar -xvf sampleArchive.tar`
    
 
## Zip
zip [option] [zipfile] [list_of_files]

Nén file : `zip sampleZipFile.zip ExampleFile.txt ExampleFile1.txt`
Giải nén : `unzip sampleZipFile.zip`
  
* `-d` : xóa 1 file từ file.zip
* `-u` : thêm file vào file né .zip
* `-r` : nén toàn bộ file bên trong một thư mục
* `-x` : nén file zip nhưng loại trừ 1 số file
    
  
## Apt
`apt-get` cung cấp các chức năng thường dùng
- **apt-get install package-name(s)** - Cài đặt gói phần mền quy định, cùng với bất kỳ phụ thuộc
- **apt-get remove package-name(s)**- Loại bỏ gói phần mềm quy định, nhưng không loại bỏ sự phụ thuộc
- **apt-get autoremove** - Loại bỏ bất kỳ phụ thuộc.
- **apt-get clean** - Loại bỏ các tập tin gói đã tải về (.deb) cho các phần mềm đã được cài đặt
- **apt-get purge package-name(s)** - Kết hợp các chức năng của loại bỏ và làm sạch cho một gói cụ thể, cũng như các file cấu hình
- **apt-get update** - Đọc tập tin /etc/apt/sources.list và cập nhật dữ liệu của hệ thống về gói sẵn để cài đặt. Chạy lệnh này sau khi thay đổi tập sources.list.
- **apt-get upgrade** - nâng cấp tất cả các gói có bản cập nhật có sẵn. Chạy lệnh này sau khi chạy apt-get update.


`apt-cache` cung cấp thêm thông tin
- **apt-cache search package-name(s)** - Nếu bạn biết tên của một phần mềm nhưng apt-get install không thành công hoặc điểm trỏ đến phần mềm sai, điều này có vẻ tên đã bị thay đổi.
- **apt-cache show package-name(s)** - Hiển thị thông tin phụ thuộc, số phiên bản và mô tả cơ bản của gói.
- **apt-cache depends package-name(s)** - Liệt kê những gói cụ thể mà phụ thuộc vào gói chính. Đây là những gói sẽ được cài đặt với apt-get install.
- **apt-cache rdepends package-name(s)** - kết quả đầu ra là một danh sách các gói mà phụ thuộc vào một gói cụ thể. Danh sách này thường xuyên có thể khá dài, vì vậy tốt nhất nên kết hợp thêm lệnh less.
- **apt-cache pkgnames** - Tạo ra một danh sách các gói cài trên hệ thống của bạn. Danh sách này thường là khá dài, vì vậy tốt nhất nên kết hợp thêm lệnh less, hoặc đưa output vào một tập tin văn bản.
  
  
  
  
## dpkg
- **dpkg -i package-file-name.deb** - Cài đặt một file .deb
- **dpkg --list search-pattern** – Liệt kê danh sách gói hiện được cài đặt trên hệ thống
- **dpkg --configure package-name(s)** - Chạy một giao diện cấu hình để thiết lập một gói.
- **dpkg-reconfigure package-name(s)** - Chạy một giao diện cấu hình trên một gói đã được cài đặt

## Cài đặt 1 chương trình từ source trên Linux
+ Cài mã nguồn của gói (định dạng file .gz hoặc .bz2)
+ Giải nén bằng gunzip hoặc bunzip2, hoặc tar -xvf, tar -zxvf
+ Tìm tập tin install có phần hướng dẫn cài đặt 
+ Hầu hết tuần tự theo các bước sau
	- ./configure
	- make
	- make install
+ Sau khi thực hiện lệnh make xong thì toàn bộ mã nguồn của gói đã được biên dịch sang dạng thực thi 
+ Nhưng các file thực thi vẫn còn trên thư mục
+ Thực hiện thêm lệnh "make install" để chép các file thực thi đó sang vị trí của nó trên hệ thống
+ /usr/bin chứa các file thực thi cho các gói đã cài đặt trên máy
  
  
  
  
  
  
  
  

