FROM debian:jessie
MAINTAINER Alexander Schenkel <alex@alexi.ch>

RUN apt-get update
RUN apt-get install -y apt-transport-https lsb-release ca-certificates wget
RUN wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
RUN echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list

RUN apt-get update && \
    apt-get install -y \
      locales \
      apache2 \
      php7.1 \
      php7.1-cli \
      php7.1-common \
      php7.1-curl \
      php7.1-gd \
      php7.1-json \
      php7.1-mbstring \
      php7.1-mysql \
      php7.1-opcache \
      php7.1-readline \
      php7.1-xml \
      php7.1-mcrypt \
      php7.1-ldap \
      php7.1-mysql \
      curl

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/bin --filename=composer

RUN a2enmod rewrite
      
CMD apachectl -DFOREGROUND