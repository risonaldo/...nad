FROM php:5.6-apache

WORKDIR /var/www/html

COPY .docker/config/php.ini $PHP_INI_DIR/php.ini
COPY .docker/config/apache2.conf /etc/apache2/apache2.conf
COPY .docker/config/ports.conf /etc/apache2/ports.conf



RUN a2enmod rewrite
RUN apache2ctl stop && apache2ctl start



# PHP extensoes
RUN docker-php-ext-install pdo 
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install mysqli 
RUN docker-php-ext-install mysql

