# Let’s Install a Full Webserver with Apache, PHP, MySQL and phpMyAdmin on our Kubuntu System!
Steps:
- sudo apt-get update
- sudo apt-get install apache2
- sudo apache2ctl configtest
- sudo nano /etc/apache2/apache2.conf
- Add ServerName 127.0.0.1/IP VPS
- sudo apache2ctl configtest
- sudo systemctl restart apache2
- sudo chmod 777 /var/www/html
- sudo apt-get install mysql-server
- sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql
- sudo nano /etc/apache2/mods-enabled/dir.conf
- change index.php
- sudo systemctl restart apache2
- cd /var/www/html
- sudo nano index.php
- php phpinfo(); 
- sudo apt-get install phpmyadmin
- sudo nano /etc/apache2/apache2.conf
- Add Include /etc/phpmyadmin/apache.conf
- sudo systemctl restart apache2
- Enjoy
- sudo apt-get install -y php-ssh2

# Konfigurasi Database
- mysql
```
CREATE USER 'namauser'@'localhost' IDENTIFIED BY 'password user';
```
* Untuk memberikan hak khusus ke akun pengguna, Anda dapat menggunakan sintaks berikut:
- GRANT permission1, permission2 ON nama_database.nama_tabel TO 'user_database'@'localhost';
# Berikut ini beberapa contohnya:
- Memberikan semua hak istimewa ke akun pengguna untuk database tertentu :
```
GRANT ALL PRIVILEGES ON nama_database.* TO 'user_database'@'localhost';
```
- Memberikan semua hak istimewa ke akun pengguna untuk semua database :
```
GRANT ALL PRIVILEGES ON *.* TO 'user_database'@'localhost';
```
- Berikan semua hak istimewa ke akun pengguna untuk tabel tertentu dari database:
```
 GRANT ALL PRIVILEGES ON nama_database.nama_tabel TO 'user_database'@'localhost';
```
- systemctl restart apache2

- https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-20-04-id
- https://aantamim.id/mengaktifkan-htaccess-apache/
