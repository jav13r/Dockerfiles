FROM php:7.2.4-cli

RUN apt-get update \
    && apt-get install -y \
    zip \
    unzip \
    curl \
    wget \
    nano \
    cron \
    git \
    libpq-dev \
    && php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
    && php composer-setup.php --install-dir=/usr/bin --filename=composer \
    && php -r "unlink('composer-setup.php');"
