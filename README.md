# speed mysql server for test

## setup mysql container

```bash
docker run --name mysql-test \
-p 3308:3306 \
-v `pwd`/mysql-test.cnf:/etc/mysql/conf.d/mysql-test.cnf \
--tmpfs /var/lib/mysql:rw \
-e MYSQL_USER=root \
-e MYSQL_ROOT_PASSWORD=unitest\
-d mysql:5.7 \
--character-set-server=utf8mb4 \
--collation-server=utf8mb4_unicode_ci
```
