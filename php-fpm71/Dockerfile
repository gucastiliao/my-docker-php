FROM php:7.1.9-fpm

RUN apt-get update \
  && docker-php-ext-install pdo_mysql mysqli mbstring

RUN apt-get update \
  && apt-get install -y git curl openssh-client zip unzip \
  && pecl install xdebug \
  && docker-php-ext-install pcntl \
  && docker-php-ext-enable xdebug \
  && docker-php-source delete \
  && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
