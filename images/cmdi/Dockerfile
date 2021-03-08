FROM centos:7

RUN yum install httpd -y

COPY site /var/www/html

COPY run.sh /run.sh

CMD sh /run.sh