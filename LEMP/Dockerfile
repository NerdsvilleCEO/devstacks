FROM php:7.4-fpm
RUN apt-get -y update \
    && apt-get -y install libfreetype6-dev libjpeg-dev libgif-dev libpng-dev zlib1g-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install pdo-mysql
