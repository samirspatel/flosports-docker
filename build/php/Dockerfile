FROM php:7.0-fpm

RUN useradd -ms /bin/bash vagrant
RUN docker-php-ext-install pdo pdo_mysql

USER vagrant
WORKDIR /app