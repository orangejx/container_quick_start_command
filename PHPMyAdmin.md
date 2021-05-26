# PHPMyAdmin
> the environment variable `MYSQL_ROOT_PASSWORD` must be consistent with those in the MariaDB container.

### Quick Start PHPMyAdmin Container
  - `docker run --name PHPMyAdmin -d --link MariaDB:db -e MYSQL_ROOT_PASSWORD="SngS67tMSxjJbiACcDXPttyi8jFnzav7" -p 8082:80 --hostname=PHPMyAdmin --restart=always phpmyadmin:5.0.4`
