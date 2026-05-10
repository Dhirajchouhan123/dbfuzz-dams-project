FROM php:7.4-apache

RUN sed -i 's/deb.debian.org/archive.debian.org/g' /etc/apt/sources.list && \
    sed -i 's/security.debian.org/archive.debian.org/g' /etc/apt/sources.list && \
    sed -i '/bullseye-security/d' /etc/apt/sources.list && \
    apt-get update --allow-insecure-repositories && \
    apt-get install -y --allow-unauthenticated \
    libzip-dev zip libpng-dev libicu-dev

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-configure zip && \
    docker-php-ext-install zip

RUN docker-php-ext-configure intl && \
    docker-php-ext-install intl

RUN docker-php-ext-install pdo pdo_mysql mysqli gd

RUN a2enmod rewrite
