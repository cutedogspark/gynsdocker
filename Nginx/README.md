# Nginx

## Parameter
```sh
PHP_UPSTREAM=php-fpm
PHP_UPSTREAM_PORT=9000
NGINX_USER_NAME=www-data
NGINX_USER_UID=1000
```

## build Nginx
```sh
docker build .

or

docker build --build-arg PHP_UPSTREAM=php-fpm PHP_UPSTREAM_PORT=9000 .
```