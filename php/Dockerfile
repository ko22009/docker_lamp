FROM debian:jessie
MAINTAINER Alexander Schenkel <alex@alexi.ch>

RUN apt-get update && \
    apt-get install -y \
      locales \
      apache2 \
      php5 \
      php5-mcrypt \
      php5-cli \
      php5-gd \
      php5-json \
      php5-ldap \
      imagemagick \
      php5-imagick \
      php5-mysql \
      php5-pgsql \
      curl \ 
      libcurl3 \
      php5-curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/bin --filename=composer

RUN a2enmod rewrite
      
CMD apachectl -DFOREGROUND