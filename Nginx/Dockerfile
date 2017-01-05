FROM nginx:alpine

MAINTAINER Chen Ming-Jui <cutedogspark@gmail.com>

ADD nginx.conf /etc/nginx/

ARG PHP_UPSTREAM=php-fpm
ARG PHP_UPSTREAM_PORT=9000
ARG NGINX_USER_NAME=www-data
ARG NGINX_USER_UID=1000

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash \
    && adduser -D -H -u ${NGINX_USER_UID} -s /bin/bash ${NGINX_USER_NAME} \
    && rm /etc/nginx/conf.d/default.conf \
    && echo "upstream php-upstream { server ${PHP_UPSTREAM}:${PHP_UPSTREAM_PORT}; }" > /etc/nginx/conf.d/upstream.conf

CMD ["nginx"]

EXPOSE 80 443