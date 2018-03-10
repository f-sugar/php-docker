FROM php:7.2.3-fpm

ADD extra-php.ini /usr/local/etc/php/conf.d/extra-php.ini

RUN mkdir /app
WORKDIR /app

RUN apt-get update && apt-get install -y git libmcrypt-dev zlib1g-dev libpq-dev zip unzip vim \
    && docker-php-ext-install pdo pdo_pgsql pdo_mysql

# composer
RUN curl -sS https://getcomposer.org/installer | php && \
    mv ./composer.phar /usr/local/bin/composer

EXPOSE 9000
