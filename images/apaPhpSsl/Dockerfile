FROM centos:7

RUN \
    yum -y install \
    httpd \
    php \
    php-cli \
    php-common \
    mod_ssl \
    openssl

COPY ssl.conf /etc/httpd/conf.d/default.conf

CMD apachectl -DFOREGROUND