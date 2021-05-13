# NextCloud
> The MySQL database used in this example comes from the MariaDB container.

### Create Docker Volume
  - `docker volume create nextcloud_data`

### Quick Start NextCloud Container
  - `docker run -d --name NextCloud --link MariaDB:db -e SMTP_HOST:smtp.qiye.aliyun.com -e SMTP_NAME:test@test.com -e SMTP_PASSWORD:"this_is_test_smtp_password" -e SMTP_SECURE:ssl -e SMTP_AUTHTYPE:login -e SMTP_PORT:465 -e MAIL_DOMAIN:test.com -e MAIL_FROM_ADDRESS:"test@test.com" -e MYSQL_HOST:db -e MYSQL_DATABASE:nextcloud -e MYSQL_USER:nextcloud -e MYSQL_PASSWORD:"this_is_test_mysql_password" -e NEXTCLOUD_ADMIN_USER:this_is_test_nc_admin_username -e NEXTCLOUD_ADMIN_PASSWORD:this_is_test_nc_admin_password -e TRUSTED_PROXIES:"10.0.0.0/8 172.16.0.0/12 192.168.0.0/16" -e REDIS_HOST:172.17.0.1 -e REDIS_HOST_PORT:6379 -v nextcloud_data:/var/www/html -p 8083:80 nextcloud`
