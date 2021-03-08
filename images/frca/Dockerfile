FROM centos:7

RUN yum install httpd -y

# COPY site /var/www/html
ADD site /var/www/html

CMD apachectl -DFOREGROUND