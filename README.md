##### MYSQL VOLUME
```
docker create -v /var/lib/mysql --name mysqldata mysql:5.7.35
```
---
##### MYSQL
```
docker run --name mysqldb --volumes-from mysqldata -e MYSQL_ROOT_PASSWORD=password -p 4000:3306 mysql:5.7.35
```
---
##### GIT IGNORE
```
docker-compose.yml
Dockerfile
mysql/*
php/*
nginx/*
```
---
##### DB CONFIG
```
DB_HOST=docker.for.mac.localhost
DB_PORT=4000
```