# Wordpress

### Create Docker Volume
  - `docker volume create wordpress_data`

### Make Directory & Create Config File
  - `cd /var/lib/docker/volumes/wordpress_data/_data`
  - `mkdir conf`
  - `mkdir data`
  - `touch conf/wordpress.ini`

### Paste Wordpress Environment Variable to Config File
```
[PHP]
memory_limit = 256M
post_max_size = 256M
upload_max_filesize = 256M
max_file_uploads = 32
date.timezone = PRC
```
  > u can change the timezone to your timezone value.

  > through the above, u can change the maximum upload file size and memory size.

  - Copy the above content and paste it into `conf/wordpress.ini` file

### Quick Start Wordpress Container
  - `docker run -d --name "Wordpress" --link MariaDB:db -e WORDPRESS_DB_HOST="db" -e WORDPRESS_DB_USER="wordpress_user" -e WORDPRESS_DB_PASSWORD="wordpress_password" -e WORDPRESS_DB_NAME="wordpress_user" -e WORDPRESS_DB_CHARSET="utf8mb4" -e WORDPRESS_DB_COLLATE="utf8mb4_unicode_ci" -e WORDPRESS_TABLE_PREFIX="wordpress_" -e WORDPRESS_DEBUG=0 -p 127.0.0.1:8081:80 -v wordpress_data/conf/wordpress.ini:/usr/local/etc/php/conf.d/wordpress.ini -v wordpress_data/data:/var/www/html --restart=always wordpress:5.7.1-php8.0-apache`
