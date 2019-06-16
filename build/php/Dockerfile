FROM php:7.0-fpm

RUN useradd -ms /bin/bash vagrant
RUN docker-php-ext-install pdo pdo_mysql

RUN apt-get update && apt-get install -y zlib1g-dev libicu-dev libpq-dev \
    && docker-php-ext-install opcache \
    && docker-php-ext-install intl \
    && docker-php-ext-install mbstring \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install pdo_pgsql \
    ## APCu
    && pecl install apcu-5.1.5 \
    && docker-php-ext-enable apcu

COPY php.ini /usr/local/etc/php/php.ini

USER vagrant
WORKDIR /app