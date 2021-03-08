FROM centos:7

LABEL version=1.0
LABEL description="This is an apache image"

RUN yum install httpd -y

COPY site /var/www/html

RUN echo $(whoami) > /var/www/html/user1.html

RUN useradd cancio

RUN chown cancio /var/www/html -R

USER cancio

RUN echo $(whoami) > /var/www/html/user2.html

VOLUME /var/www/html

USER root

CMD apachectl -DFOREGROUND