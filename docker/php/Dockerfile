ARG PHP_FPM_VERSION
FROM php:${PHP_FPM_VERSION}-fpm

# install composer
COPY --from=composer:1.9.1 /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
#    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install pdo_mysql

# set recommended PHP.ini settings
COPY conf.d/* /usr/local/etc/php/conf.d/
CMD  ["php-fpm"]
