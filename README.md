# Cơ bản về Ổ đĩa cứng (HDD)

### 1. Khái niệm

`Ổ đĩa cứng (HDD)` là thiết bị dùng để lưu trữ dữ liệu và là một thành phần không thể thiếu của máy tính.

### 2. Cấu tạo

#### a. Đĩa từ

- Là nơi lưu trữ dữ liệu
- Được cấu tạo bằng nhôm hoặc thủy tinh, bề mặt có phủ vật liệu từ tính
- Ở mỗi ổ cứng, số lượng đĩa có thể nhiều hơn 1, phụ thuộc vào dung lượng của ổ và công nghệ của hãng sản xuất
- Trong ổ cứng, các đĩa từ được gắnsong song, quay đồng trục và quay cùng một tốc độ khi hoạt động

###### *Sector*

- Là các phần nhỏ trên track, để chứa dữ liệu. Thông thường, một sector chuẩn chứa được 512 Byte dữ liệu

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/sector_zpsigjzdeaf.png" />

###### *Track*

- Là các đường tròn đồng tâm trên mặt đĩa từ
- Các track ở trên ổ thường không cố định khi sản xuất, chúng có thể bị thay đổi vị trí khi low format.

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/track_zps83pglrgk.png" />

###### *Cylinder*

- Là tập hợp các track có cùng bán kính, nằm trên các đĩa khác nhau

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/cylinder_zpsxrsypd4n.png" />

#### b. Trục quay

- Là một trục thẳng đứng dùng để gắn các đĩa từ và được nối trực tiếp với động cơ
- Nhiệm vụ chính của nó là truyền chuyển động quay cho các đĩa từ

#### c. Đầu đọc/ghi

- Nhiệm vụ chính của nó là đọc/ghi dữ liệu lên đĩa từ

#### d. Cần di chuyển đầu đọc/ghi
 
- Di chuyển đầu đọc đến các vị trí trên đĩa từ

<img src="http://www.helpdisc.hr/gallery/HDD%20Head.jpg" width=40% height=40% ></img>

*Hình ảnh Đầu đọc/ghi và Cần di chuyển*

#### 3. Chia Partition với `parted` và `fdisk`

##### `parted` trên Ubuntu 14.0.4 Server

Khi gắn ổ cứng mới vào, ta phải gắn nhãn (lable)
Dùng lệnh `help mklable` để biết thêm chi tiết

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/parted_zpsadwltzqq.png" />

Dùng lệnh mkpart để tạo partition mới

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/parted-2_zpspyn7w6me.png" />

Ở đây, ta chỉ có thể tạo 4 Primary Partition. Để tạo hơn 4 Partition, chúng ta phải tạo 1 Extended partition.

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/parted-extended_zpsjkx9gzhf.png" />

###### Tạo ổ Logical

(Các ổ Logical có tổng dung lượng bằng ổ Extended)

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/parted-extended-2_zpsq04rikwu.png" />

#### `fdisk` 
Chia ổ ở fdisk, sau khi chia xong bấm `w` để lưu lại những gì đã thao tác.

<img src="http://i1363.photobucket.com/albums/r714/HoangLove9z/disk/fdisk-2_zpssg3xlvyg.png" />
