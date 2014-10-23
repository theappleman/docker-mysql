FROM applehq:client

MAINTAINER Daniel Cordero <docker@xxoo.ws>

RUN yum install -y epel-release
RUN yum install -y holland-mysqldump

RUN holland mc mysqldump > /etc/holland/backupsets/default.conf
