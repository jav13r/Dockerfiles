FROM php:7.0.30-fpm

ENV TERM xterm 

RUN apt-get update \
    && apt-get install -y \
    cron \
    nano \
    bzip2 \
    wget \
    libpq-dev \
    libxslt1.1 libxslt1-dev \
    libfreetype6-dev \
    libicu-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng12-dev \
    supervisor \
    libxml2-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-configure gd \
    --with-gd \
    --with-freetype-dir=/usr/include/ \
    --with-jpeg-dir=/usr/include/ \
    --with-png-dir=/usr/include \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install -j$(nproc) iconv intl mcrypt mbstring opcache xsl zip  \
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo pdo_pgsql pgsql soap \
    && pecl install redis && docker-php-ext-enable redis
