FROM php:7.4-fpm

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install mysqli

RUN pecl install redis-5.1.1 \
    && pecl install xdebug-2.8.1 \
    && docker-php-ext-enable redis xdebug
RUN docker-php-ext-install bcmath pdo_mysql