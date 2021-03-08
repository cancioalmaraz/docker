FROM nginx

RUN useradd cancio

COPY site /usr/share/nginx/html

ENV archivo=docker

WORKDIR /usr/share/nginx/html

RUN echo "$archivo" > /usr/share/nginx/html/env.html

EXPOSE 90

LABEL version="1.0"

USER cancio

RUN echo "Yo soy $(whoami)" > /tmp/i.html

USER root

RUN cp /tmp/i.html /usr/share/nginx/html/docker.html

VOLUME /var/log/nginx

CMD nginx -g 'daemon off;'