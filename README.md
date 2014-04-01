Tự động cài đặt NGINX,PHP-FPM, MySql, phpMyAdmin trên CentOS VPS với ComfortVPS Script
==========================

############ Các tính năng chính của script

- Tự động cài đặt phiên bản mới nhất của Nginx1.4.x, PHP5.x, MySql5.x
- Tự động cài đặt phpMyAdmin4.x
- Có thể thêm website trực tiếp thông qua SFTP, không cần phải login SSH, không cần khởi động lại Nginx.
- Có thể dễ dàng tùy chỉnh file cấu hình Nginx cho các domain nếu cần.
- Hoạt động tốt với các VPS cấu hình thấp, kể cả các VPS chỉ có 128MB RAM.

############ Yêu cầu hệ thống

 - OS: Script chỉ hoạt động trên hệ điều hành CentOS 5.x/6.x 32bit hoặc 64bit. Bạn nên reload hệ điều hành trước khi sử dụng csript.
 - RAM: Script chạy tốt trên VPS Xen 128MB RAM. Tuy nhiên, tốt nhất bạn cần có 256 MB RAM đối với hệ thống cài CentOS 32 bit và 512 MB RAM đối với hệ thống cài CentOS 64 bit. Đối với VPS được ảo hóa trên nền tảng OpenVZ, khuyến cáo nên có ít nhất 512MB RAM.
 - Dung lượng ổ cứng: Còn trống ít nhất 2Gb.
 - Bạn cần đăng nhập được vào VPS bằng quyền root.

############ Cài đặt

Kết nối với VPS của bạn bằng SSH hoặc Putty và chạy một câu lệnh duy nhất:

wget -O /tmp/install-nginx-php-mysql.sh https://raw.github.com/EXAtrueCloud/Nginx-PHP-MySql-phpMyAdmin/master/install-nginx-php-mysql.sh; sh /tmp/install-nginx-php-mysql.sh;

Việc cài đặt sẽ diễn ra hoàn toàn tự động, mất khoảng từ 5 đến 15 phút, bạn không phải làm gì thêm cả.

Khi cài đặt hoàn thành, các thông tin về kết quả cài đặt sẽ được đưa ra màn hình. Cụ thể như sau:

====== Nginx + PHP-FPM + MYSQL Successfully installed

====== MySql root password is lw7t2thgexu=  #Mật khẩu đăng nhập MySQL cho tài khoản root

====== SFTP Username is myweb   # Tài khoản đăng nhập SFTP là myweb

====== SFTP Password is lw7t2thgexu=  # Mật khẩu đăng nhập SFTP với tài khoản myweb là cft.lw7t2thg

====== Website document root is /www/yourdomain   # Thư mục web

====== Now you can visit http://your-ip-address/

====== Eg. http://192.30.34.46 /    # Bạn có thể truy cập vào địa chỉ IP để test

====== phpMyAdmin: http://192.30.34.46 /phpMyAdmin/  # Địa chỉ truy cập vào phpMyAdmin.

Hãy thử truy cập vào VPS qua địa chỉ IP, ví dụ http://192.30.34.46 /, bạn sẽ thấy webserver đã chạy sẵn sàng.


################## Cách thêm nhiều website (tên miền) thông qua SFTP? 

Bước 1, Đăng nhập SFTP -> Tạo một thư mục tên miền trong thư mục /www ví dụ như: yourdomain.com, subdomain.abc.com, domain-name.net 

Bước 2, Trỏ tên miền về IP máy chủ, tải lên các tập tin php/html của bạn vào thư mục tên miền mà bạn đã tạo để thử nghiệm.


