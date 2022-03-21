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

## Chương trình nén và giải nén trong linux
+ Nén file có đuôi .gz <gzip>
    - Nén: gzip <tên file>
    - Kiểm tra: gzip -l <ten file đã nén> 
    - Giải nén: gzip -d filename
+ Zip
    -Nén: zip filename.zip filename1 filename2: filename.zip là file zip được tạo từ việc nén filename1 và filename2
    - zip -r test.zip folder1: nén toàn bộ folder và các file bên trong
    - Giải nén: unzip filename
+ Tar
        - c: tạo file lưu trữ
        - x: giải nén file lưa trữ
        - z: nén với gzip
        - j: nén với bunzip2
        - f: chỉ đến file lưu trữ sẽ tạo
        - v: hiện thị tập tin đang làm việc lên màn hình
    -  Giải nén file tar: tar -xvf filename.tar
    - Với file nén zip: tar -xzvf filename.tar.gz
                  tar -xjvf filename.tar.bz2

  
 ## Tar
 Tape archive, là một lệnh phổ biến nhất để nén và giải nén file và thư mục trong Linux
 
 - **c** : tạo file .tar mới
 - **v** : 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

