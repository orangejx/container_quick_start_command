# MariaDB

### Create Docker Volume
  - `docker volume create mariadb_data`

### Quick Start MariaDB Container
  - `docker run --name MariaDB -v mariadb_data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD="SngS67tMSxjJbiACcDXPttyi8jFnzav7" -p 127.0.0.1:3306:3306 -d mariadb:10.5.8 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci`
