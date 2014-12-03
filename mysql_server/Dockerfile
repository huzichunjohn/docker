FROM centos:centos6
MAINTAINER huzichun

RUN yum -y install mysql mysql-server

RUN /etc/init.d/mysqld start && \
    mysql -e "grant all privileges on *.* to 'root'@'%' identified by '123456';" && \
    mysql -e "grant all privileges on *.* to 'root'@'localhost' identified by '123456';" && \
    mysql -u root -p'123456' -e "show databases;"

EXPOSE 3306

CMD ["/usr/bin/mysqld_safe"]
