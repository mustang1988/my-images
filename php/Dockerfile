FROM php:7.1.4-fpm-alpine
RUN apk update \
    && apk add --no-cache \
        $PHPIZE_DEPS openssl-dev pcre-dev supervisor dcron libpng-dev libjpeg libmcrypt-dev libxml2-dev \
    && pecl channel-update pecl.php.net \
    && pecl install mongodb \
    && pecl install redis \
    && docker-php-ext-install bcmath exif mcrypt mysqli pdo_mysql shmop soap sockets sysvsem xmlrpc zip \
    && docker-php-ext-configure gd --with-jpeg-dir=/usr/lib \
    && docker-php-ext-install gd \
    && docker-php-ext-enable bcmath exif gd mcrypt mysqli pdo_mysql shmop soap sockets sysvsem xmlrpc zip mongodb redis \
    && apk del $PHPIZE_DEPS \
    && apk del openssl-dev \
    && apk del pcre-dev \
    && rm -rf /tmp/pear/* \
    && rm -rf /var/cache/apk/*