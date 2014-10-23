docker-mysql
============

MySQL server, cli clients and holland backups in docker containers

Getting Started
---------------

```
$ docker run -v /data/mysql:/var/lib/mysql applehq/mysql:server mysql_install_db
# chown -R 27:27 /data/mysql
$ docker run -d -v /data/mysql:/var/lib/mysql applehq/mysql:server mysqld_safe --user=mysql

$ docker run -it -v /data/mysql/mysql.sock:/var/lib/mysql/mysql.sock applehq/mysql:server mysql_secure_installation

# touch /var/log/holland.log
$ docker run -v /var/log/holland.log:/var/log/holland/holland.log -v /var/lib/mysqlbackup:/var/spool/holland -v /data/mysql/mysql.sock:/var/lib/mysql/mysql.sock applehq/mysql:holland holland bk
```
