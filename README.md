<h3 align="left">Sinh viên: Trịnh Văn Khánh - 21020343</h3>

<h2 align="center">- MỤC LỤC -</h2>
<h3 align="left">Phần 1: Bài tập lý thuyết</h3>

  [1. Docker và Docker-compose?](#1) 

  [2. Linux vs Unix vs BSD vs *nix? MacOS thuộc loại nào?](#2)

  [3. Alpine và Ubuntu ?](#3)

  [4. VNC ?](#3)
<h3 align="left">Phần 2: Bài tập thực hành</h3>

[1. Các bước thực hiện](#5) 

[2. Minh chứng](#6) 
<h1 align="center">Phần 1: Câu hỏi tìm hiểu</h1>

<a name="1"></a>
## 1. Docker và Docker-compose?
<a name="1.1"></a>
### 1.1. Docker
  Một nền tảng Containerization, đóng gói ứng dụng và các phụ thuộc của nó vào một container độc lập. Container này chứa môi trường và tài nguyên cần thiết để ứng dụng hoạt động một cách tin cậy và nhất quán trên mọi máy chủ.
<a name="1.2"></a>
### 1.2. Docker-compose
- Công cụ giúp định nghĩa và quản lý các ứng dụng multi-container, sử dụng một tệp YAML/JSON để mô tả cấu hình của các container, network và lưu trữ dữ liệu.
  
- Docker-compose giải quyết vấn đề việc lập trình viên thay vì phải xây dựng (rất) nhiều containers tương ứng với các modules (frontend, backend, database,...) bằng cách cấu hình một file duy nhất.

<a name="2"></a>
## 2. Linux vs Unix vs BSD vs *nix? MacOS thuộc loại nào?
<a name="2.1"></a>
### 2.1. Unix
- Hệ điều hành máy tính đa nhiệm, có đặc điểm là thiết kế theo module, hệ điều hành cung cấp một tập hợp các công cụ đơn giản, mỗi công cụ chỉ thực hiện những chức năng giới hạn và được định nghĩa rõ ràng, có khả năng bảo mật cao, tương thích nhiều thiết bị và cung cấp khả năng tùy chỉnh linh hoạt tuy nhiên unix có nhược điểm về giao diện, sự phức tạp của các tập lệnh và việc cài đặt các phần mềm.

- Hiện nay UNIX được sử dụng bởi nhiều công ty tập đoàn lớn trên thế giới vì mức độ bảo mật của nó tương đối cao, được phát triển thành nhiều phiên bản sử dụng trên nhiều môi trường phần cứng khác nhau. Các phiên bản UNIX hiện nay có thể kể đến: HP-UX (HP), AIX (IBM), Solaris (Sun/Oracle), Mac OS X (Apple).
<a name="2.2"></a>
### 2.2. Linux
- (GNU/Linux) - Hệ điều hành mã nguồn mở, miễn phí nhằm thay thế môi trường UNIX thương mại. Phiên bản Linux đầu tiên do Linus Torvalds viết vào năm 1991 bằng ngôn ngữ C. Linux có tính bảo mật cao và linh hoạt, người dùng có thể chỉnh sửa hệ điều hành để phù hợp với nhu cầu sử dụng của mình (phù hợp với các developers). Tuy nhiên việc cài đặt và sử dụng linux sẽ gặp nhiều khó khăn.

| Tiêu chí đánh giá | UNIX  | LINUX | 
|-------------------|-------|-------|
| **Kiến trúc phần cứng** | Được lập trình để chạy trên một nhóm kiến trúc phần cứng nhất định. Việc giới hạn phần cứng giúp các công ty bán UNIX tối ưu hóa HĐH của mình để có thể chạy thật tốt trên một thiết bị phần cứng nào đó. | Có thể chạy trên rất nhiều kiến trúc phần cứng, và số lượng các thiết bị gán ngoài, thiết bị I/O hầu như không giới hạn. Do đó cũng dấn tới hệ quả là không thể hoàn toàn tối ưu hóa HĐH cho từng kiến trúc phần cứng. |
| **Hệ thống file** | Định dạng file jfs, gpfs, hfs, hfs+, ufs, xfs, zfs | Định dạng file Ext2, Ext3, Ext4, Jfs, ReiserFS, Xfs, Btrfs, FAT, FAT32, NTFS |
| **Nhân Hệ điều hành** | Thường được cung cấp dưới dạng nhị phân hay các gói "nguyên khối", và những người khác chỉ có thể nâng cấp, chỉnh sửa một phần nhỏ. Thường có tính đóng. | Nhân Linux và và các thành phần khác đều là phần mềm tự do và mã nguồn mở. Nên việc biên tập, vá lỗi kernel và driver dễ dàng hơn. Do đó, khi có bug lỗi xảy ra thì tự người dùng có thể fix hoặc được hỗ trợ fix nhanh chóng thông qua các forum Open source|
|**Phát hiện và xử lý lỗi**| Do tính chất độc quyền của UNIX nên khi phát hiện mỗi đe dọa hay lỗi thì người dùng phải chờ đợi một thời gian để được các nhà cung cấp hỗ trợ. Nhưng thường không hay xảy ra vấn đề này. | Việc phát hiện các mối đe dọa hay các lỗi thường được phát hiện và cũng hầu như cũng tìm được giải pháp giải quyết rất nhanh bởi cộng đồng người dùng Open Source. |

<a name="2.3"></a>
### 2.3. BSD - Berkeley Software Distribution
- Là phiên bản Unix cho những tổ chức giáo dục được xây dựng bởi Computer Systems Research Group ban đầu dựa trên codebase và design của Unix sau đó mở rộng thêm FreeBSD, NetBSD và OpenBSD. Phiên bản thương mại, close source nổi tiếng là MacOS của Apple. MacOS cũng như các hệ điều hành khác của Apple hiện nay là iOS, watchOS, và tvOS đều được dựa trên nền tảng của BSD. MacOS cũng là một trong số ít các hệ điều hành được coi là Unix-like, khi có được chứng nhận Single UNIX Specification.
<a name="2.4"></a>
### 2.4. *nix - Unix like
- Khái niệm "Unix-like" dùng để chỉ những hệ điều hành có được chứng nhận SUS Single UNIX Specification và có thể sử dụng thương hiệu UNIX, ngoài ra có ý kiến Unix-like có thể định nghĩa làm 3 loại:
  - Genetic UNIX: Chỉ những hệ điều hành có liên quan trực tiếp đến codebase của phiên bản Unix của Bell Labs.
  - Trademark UNIX: Những hệ điều hành thỏa mãn yêu cầu SUS và có thể sử dụng thương hiệu UNIX.
  - Functional UNIX: Những hệ điều hành "hoạt động giống Unix", và Linux có thể được xếp vào loại này.
<a name="2.5"></a>
### 2.5. MacOS thuộc hệ điều hành nào ?
 Như đã trình bày trong mục 2.3, MacOS cũng là một trong số ít các hệ điều hành được coi là Unix-like (*nix) dựa trên nền tảng của BSD.
<a name="3"></a>
## 3. Alpine và Ubuntu ?
<a name="3.1"></a>
### 3.1. Alpine - Alpine Linux
- Là bản phân phối Linux dựa trên musl và BusyBox, được thiết kế bảo mật, đơn giản và hiệu quả về tài nguyên,sử dụng OpenRC chạy các ứng dụng trên linux distribution. Alpine được thiết kế để chạy trực tiếp từ RAM, không chỉ cung cấp một môi trường Linux chính thức mà còn cung cấp một danh sách các packages.nó nhỏ hơn và hiệu quả hơn các hệ điều hành dựa trên GNU/LINUX truyền thống như Ubuntu. Do đó khi nền tảng containerization như docker xuất hiện, Alpine hường được sử dụng làm docker image.
<a name="3.2"></a>
### 3.2. Ubuntu
  Ubuntu là một linux distribution dựa trên Debian GNU/LINUX được sử dụng rộng rãi, hỗ trợ thư viện GNU/C và có các công cụ quản lý packages dựa trên APT, sử dụng giao diện đồ họa thân thiện GNOME, hướng đến sự đơn giản hóa trong quá trình sử dụng. Ngoài ra, Ubuntu còn có bộ ứng dụng văn phòng OpenOffice, trình duyệt Firefox, trình gửi tin nhắn tức thời Pidgin, trình biên tập đồ họa GIMP.
## 4. VNC - Virtual Network Computing
- Là một công nghệ dùng để chia sẻ giao diện màn hình từ xa (remote desktop sharing). VNC giúp người dùng kết nối máy tính từ xa, quản lý, theo dõi,... từ các phương tiện như laptop, điện thoại thông minh. Tuy nhiên VNC nói riêng phụ thuộc vào đường truyền mạng, hiệu suất thao tác đôi khi hơi chậm và không ổn định và độ bảo mật không cao

- VNC hoạt động theo cơ chế client/server và sử dụng giao thức VNC khá đơn giản, giao thức này chỉ phục vụ một mục đích duy nhất đó là truy cập kênh giao diện đồ hoạ của máy tính người dùng từ xa qua mạng, được thiết kế dựa trên ý tưởng của Remote Frame Buffer (RFB). VNC Client (viewer) sẽ chia sẻ các input như (bàn phím, di chuyển chuột, click chuột,…) với VNC Server. VNC Server sẽ ghi lại các nội dung hiển thị framebuffer và chia sẻ chúng lại cho VNC Client.

<h1 align="center">Phần 2: Bài tập thực hành</h1>

<a name="5"></a>
## 1. Các bước thực hiện
(Cần đảm bảo đã cài đặt và chạy thành công Docker, docker-compose)
### Bước 1: Viết Dockerfile, docker-compose.yml
- Dockerfile này sử dụng base image ubuntu, cài đặt ssh và mở cổng truy cập từ localhost. Chi tiết được comment trong file Dockerfile.
- Để sử dụng docker-compose cần có thêm file docker-compose.yml, cấu hình các services và các cổng ánh xạ đến containers.
### Bước 2: Chạy image
- Sử dụng câu lệnh ```docker compose up -d``` để chạy image
- Kiểm tra container running thành công bằng câu lệnh ```docker container ls```
![image](https://github.com/TKSkygod/SoftwareArchitecture_Week1/assets/89265725/dced071d-4093-4034-b04e-cf27083ddc62)
### Bước 3: Sử dụng SSH truy cập máy ảo, cài Desktop Environment xfce
- ```ssh -p 2224 root@localhost``` để ssh từ xa (tài khoản root) vào máy ảo, trong đó "-p" là cổng đã cài đặt trong docker-compose.yml
- Cài đặt XFCE Desktop Environment:
```
sudo apt update
sudo apt install xfce4 xfce4-goodies
```
- Cài đặt TightVNC Server
```
sudo apt install tightvncserver
```
![image](https://github.com/TKSkygod/SoftwareArchitecture_Week1/assets/89265725/a9687358-9c0a-4a08-9cc4-f579d6fc31ee)

- Khởi động VNC Server và Cài đặt mật khẩu mới truy cập vnc
```
vncserver
```
Sau khi cài đặt mật khẩu thành công, khởi động lại VNC server để áp dụng cài đặt ```vncserver -kill :1```
![image](https://github.com/TKSkygod/SoftwareArchitecture_Week1/assets/89265725/892d1fc2-4096-453c-a7c6-4d502ac45bae)

- (Tùy chọn) Cấu hình VNC Server
Khởi động tự động VNC-Server khi máy chủ khởi động
```
echo "#!/bin/sh" > ~/.vnc/xstartup
echo "xrdb $HOME/.Xresources" >> ~/.vnc/xstartup
echo "startxfce4 &" >> ~/.vnc/xstartup
chmod +x ~/.vnc/xstartup
```
### Bước 4: Khởi động VNC Server, thực hiện remote qua VNC Viewer
Chạy ```vncserver``` tại ssh, mở ứng dụng VNC Viewer, nhập địa chỉ localhost:"PORT" với PORT ánh xạ trong docker-compose.yml. Example localhost:5901. Sau đó nhập mật khẩu ở bước 3 để kết nối.
![image](https://github.com/TKSkygod/SoftwareArchitecture_Week1/assets/89265725/7ddfa5b2-9986-4951-9517-60f492628d3a)

<a name="6"></a>
## 2. Kết quả
![image](https://github.com/TKSkygod/SoftwareArchitecture_Week1/assets/89265725/d16e00c7-bc5f-4301-9ea4-a8a57d38699e)











