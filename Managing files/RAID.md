# RAID (Redundant Arrays of Independent Disks)
![](https://f6-zpcloud.zdn.vn/4718691642337963992/b5939e95ae0a6154381b.jpg)

RAID là một kỹ thuật sử dụng kết hợp nhiều ổ đĩa vật lý lại với nhau thay vì sử dụng một đĩa duy nhất để tăng hiệu suất, dự phòng dữ liệu hoặc cả hai

- **Parity**: Tạo lại nội dung bị mất từ thông tin parity. (RAID5 và RAID6)
- **Stripe**: chia sẻ dữ liệu ngẫu nhiên nhiều đĩa
- **Mirroring**: Sử dụng trong RAID1 và RAID10. Tạo ra bản sao cùng 1 dữ liệu
- **Hot spare**: Ổ đĩa dự phòng trong máy chủ có thể tự động thay thế các ổ bị lỗi.
- **Chunks**: một kích thước của dữ liệu có thể tối thiểu từ 4Kb trở lên.


## RAID 0 - Stripping
![](https://f7-zpcloud.zdn.vn/2899105625688793956/2358318e55119a4fc300.jpg)

- RAID0 (Striping) : dữ liệu được ghi vào đĩa theo phương pháp chia sẻ
- Một nửa nội dung nằm ở 1 đĩa còn nửa còn lại nằm ở đĩa khác. Ví dụ có 8 đoạn dữ liệu được đánh số từ 1 đến 8, các đoạn đánh số lẻ (1,3,5,7) sẽ được ghi lên đĩa cứng đầu tiên và các đoạn đánh số chẵn (2,4,6,8) sẽ được ghi lên đĩa thứ hai.
- Cho phép ghi và đọc được hoàn thành nhanh hơn 
- **Độ tin cậy = 0** Không có tính parity hay khả năng dự phòng, nguy cơ mất dữ liệu (nếu 1 đĩa cứng trục trặc thì thông tin coi như không thể đọc được)
- Thích hợp cho những người dùng cần truy cập nhanh khối lượng dữ liệu lớn, ví dụ các game thủ hoặc những người chuyên làm đồ hoạ, video số


## RAID 1 - Mirroring
![](https://f5-zpcloud.zdn.vn/8655457550298645458/fd01a83e10a1dfff86b0.jpg)

Đây là dạng RAID cơ bản nhất có khả năng đảm bảo an toàn dữ liệu. Cũng giống như
RAID 0, RAID 1 đòi hỏi ít nhất hai đĩa cứng để làm việc. Dữ liệu được ghi vào 2 ổ giống 
hệt nhau (Mirroring). Trong trường hợp một ổ bị trục trặc, ổ còn lại sẽ tiếp tục hoạt động 
bình thường.

Chi phí đắt đỏ (Hiệu suất của hệ thống không đổi) , Tốc độ ghi chậm vì phải thực hiện 2 lần , ...

## RAID 5 
![](https://f7-zpcloud.zdn.vn/364288144688300577/8af9cbfd685ba705fe4a.jpg)

Đây có lẽ là dạng RAID mạnh mẽ nhất cho người dùng văn phòng và gia đình với 3 hoặc 5 đĩa cứng riêng biệt. Dữ liệu và bản sao lưu được chia lên tất cả các ổ cứng

Ví dụ về 8 đoạn dữ liệu (1-8) và giờ đây là 3 ổ đĩa cứng. Đoạn dữ liệu số 1 và số 2 sẽ được ghi vào ổ đĩa 1 và 2 riêng rẽ, đoạn sao lưu của chúng được ghi vào ổ cứng 3. Đoạn số 3 và 4 được ghi vào ổ 1 và 3 với đoạn sao lưu tương ứng ghi vào ổ đĩa 2. Đoạn số 5, 6 ghi vào ổ đĩa 2 và 3, còn đoạn sao lưu được ghi vào ổ đĩa 1 và sau đó trình tự này lặp lại, đoạn số 7,8 được ghi vào ổ 1, 2 và đoạn sao lưu ghi vào ổ 3 như ban đầu. 

Như vậy RAID 5 vừa đảm bảo tốc độ có cải thiện, vừa giữ được tính an toàn cao. Dung lượng đĩa cứng cuối cùng bằng tổng dung lượng đĩa sử dụng trừ đi một ổ.





























