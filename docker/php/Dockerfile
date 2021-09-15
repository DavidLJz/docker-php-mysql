ARG php_version

FROM php:${php_version}

RUN apt update

RUN apt install git nano less libcurl4-gnutls-dev curl libicu-dev libmcrypt-dev libvpx-dev libjpeg-dev libpng-dev libxpm-dev zlib1g-dev libfreetype6-dev libxml2-dev libexpat1-dev libbz2-dev libgmp3-dev libldap2-dev unixodbc-dev libpq-dev libaspell-dev libsnmp-dev libpcre3-dev libtidy-dev libzip-dev -yqq

RUN docker-php-ext-install mysqli pdo pdo_mysql mbstring curl json intl gd xml zip bz2 opcache
RUN a2enmod rewrite

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

COPY conf.d/* /usr/local/etc/php/conf.d/
COPY custom-scripts/* /usr/bin/