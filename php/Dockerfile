#FROM 10.7.12.3:5000/dev/php:7.1.4-supervisor-crond
FROM hub.c.163.com/mustang1988/php:7.1.4-fpm-supervisor-crond
RUN apk update \
    && apk add --no-cache libpng-dev libjpeg libmcrypt-dev libxml2-dev pcre-dev \
    && docker-php-ext-install bcmath exif gd mcrypt mysqli pdo_mysql shmop soap sockets sysvsem xmlrpc zip \
    && docker-php-ext-enable bcmath exif gd mcrypt mysqli pdo_mysql shmop soap sockets sysvsem xmlrpc zip \
    && apk del $PHPIZE_DEPS \
    && rm -rf /tmp/pear/* \
    && rm -rf /var/cache/apk/*



#        && apk del libmcrypt-dev \
#    && apk del libxml2-dev \
#    && apk del pcre-dev \