FROM php:8.2.20-fpm-alpine

RUN curl -sSLf \
    -o /usr/local/bin/install-php-extensions \
    https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions && \
    chmod +x /usr/local/bin/install-php-extensions

RUN install-php-extensions \
    bcmath \
    gd \
    imagick \
    opcache \
    pdo_mysql \
    redis \
    zip

RUN curl -sSLf \
    -o /usr/local/bin/composer \
    "https://mirrors.aliyun.com/composer/composer.phar?file=composer.phar" && \
    chmod +x /usr/local/bin/composer

RUN apk update \
    && apk add \
    supervisor \
    nginx