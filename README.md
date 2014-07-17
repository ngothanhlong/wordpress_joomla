
=========

# Hướng dẫn cài đặt và sử dụng wordpress.

  - 1.Tìm hiểu về CMS Wordpress
  - 2.Cài đặt  server tren ubuntu 12.04
  - 3.Cài đặt wordpress

#### 1.Tìm hiểu vế CMS Wordpress: 

##### a.Wordpress là gì?

> WordPress là một CMS, một mã nguồn mở và hoàn toàn miễn phí để làm blog, trang web 
> cá nhân hoặc bất cứ gì mà bạn thích. WordPress được viết bằng ngôn ngữ lập trình PHP 
> và sử dụng MySQL database. WordPress là “con” của B2 / Cafelog, được xây dựng trên sự 
> tiện dụng, cùng các định dạng chuẩn của web.

> Đơn giản ta có thể biết đến wordpress như một công cụ giúp ta tao lên các trang web cá nhân một cách đơn giản nhât.


#####b.Các điểm nổ bật : 

> - Hệ thống Plugin phong phú và cập nhật liên tục, bạn cũng có thể tự viết plugin cho mình
> - Hỗ trợ đa ngôn ngữ.
> - Được cập nhật ,vá lỗi và phát triển liên tục
> - Dễ dàng quản lý và thao tác, việc quản lý blog, bài viết giống như các phần mềm thiết kế web chuyên nghiệp.
> - Có một hệ thống Widget đa dạng ( ứng dụng tạo thêm ) như Thống kê số người truy cập, Danh sách các bài viết mới, các bài viết nổi bật, được xem nhiều, được comment nhiều, Liệt kê các chuyên mục, Liệt kê các trang, Bài viết theo ngày tháng, … có đến trên 23 Widget để bạn tha hồ lựa chọn.
> - Hệ thống phân quyền với nhiều cấp độ khác nhau như: Administrator, Author, Editor, Contributer, Subcriber. Mỗi phân quyền sẽ có các quyền hạn khác nhau như được phép đăng bài viết, sửa bài viết, xóa bài viết, duyệt comment …
> -Sao lưu dữ liệu một cách dễ dàng để backup hoặc chuyển nhà sang một nơi khác.
> -Hỗ trợ import đa năng từ các blog khác như Blogspot, Tumblr, Blogger, LiveJournal …

####2. Hướng dẫn cài server trên ubuntu server 12.04:
#####a. Cập nhật hệ thống và cài đặt apache2:

 ```sh
   sudo  apt-get udate 
   sudo apt-get install apache2 -y
```

Sau khi tải và cài apache2. Truy cập vào địa chỉ:
```sh
 https://localhost
```
 nếu  hiển 'Its work' thì bạn đã cài đặt thành công Apache2.
 
 Các lệnh quản lý Apache: 
  
  ```
     sudo service apache2 restart
     sudo service apache2 stop
     sudo service apache2 start
  ```
 OK.Vậy là xong một phần
 
 #####b.Cài Mysql-server:
 
  Câu lệnh:
   ```
     sudo apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql

   ```
  Khởi động lai Apache:
   ```sh
     sudo service apache2 restart
   ```
 
 
 #####c. Cài đặt php:
 
 
 
 ```
    sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
     
 ```
 
 Cài đặt các gói phụ thuộc cho php
 
  tìm kiếm  các gói phụ thuộc cần thiết :
  ```
      sudo apt-cache search php-*
      
  ```
  
  Bạn sẽ được một danh sách các gói phụ thuộc có thể cài đi kèm với php :
  
  ```
         php5-cgi - server-side, HTML-embedded scripting language (CGI binary)
         php5-cli - command-line interpreter for the php5 scripting language
        php5-common - Common files for packages built from the php5 source
        php5-curl - CURL module for php5
        php5-dbg - Debug symbols for PHP5
        php5-dev - Files for PHP5 module development
        php5-gd - GD module for php5
        php5-gmp - GMP module for php5
        php5-ldap - LDAP module for php5
        php5-mysql - MySQL module for php5
        php5-odbc - ODBC module for php5
        php5-pgsql - PostgreSQL module for php5
        php5-pspell - pspell module for php5
        php5-recode - recode module for php5
        php5-snmp - SNMP module for php5
        php5-sqlite - SQLite module for php5
        php5-tidy - tidy module for php5
        php5-xmlrpc - XML-RPC module for php5
        php5-xsl - XSL module for php5
        php5-adodb - Extension optimising the ADOdb database abstraction library
        php5-auth-pam - A PHP5 extension for PAM authentication
        [...]
  ```
  
  
  
  . Ở đây, tôi cài  gói liên kết với mysql :
  

  
  ```
     sudo apt-get install php-mysql -y 
  ```
  
  Sau khi cài đặt xong php. Để kiểm tra và xem thông tin của php:
  
  ```
     cd /var/www/html
     sudo vi info.php
  ```
  Trong file [@info.php] ta viết như sau:
  ```
    <?php 
      phpinfo();
    ?>
  ```
  
  
  
 
 
 
 
 
 
 
 


