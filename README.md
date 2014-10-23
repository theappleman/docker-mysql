docker-mysql
============

MySQL server, cli clients and holland backups in docker containers

Getting Started
---------------

```
$ docker run -v /data/mysql:/var/lib/mysql applehq/mysql:server mysql_install_db
# chmod -R 27:27 /data/mysql
$ docker run -d -v /data/mysql:/var/lib/mysql applehq/mysql:server mysqld_safe --user=mysql

$ docker run -v /data/mysql/mysql.sock:/var/lib/mysql/mysql.sock applehq/mysql:client mysql_secure_installation

$ docker run -v /data/mysql/mysql.sock:/var/lib/mysql/mysql.sock applehq/mysql:holland holland bk
```
