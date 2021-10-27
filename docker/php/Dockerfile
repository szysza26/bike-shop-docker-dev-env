FROM php:7.4-apache
COPY ./apache2.conf /etc/apache2/
COPY ./000-default.conf /etc/apache2/sites-available/

RUN apt-get update \
  && apt-get install -y \
        libzip-dev \
        zip \
        sqlite3 \
	openssl \
  && docker-php-ext-install \ 
	zip \
	pdo pdo_mysql \
  && a2enmod rewrite
