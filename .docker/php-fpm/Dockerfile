FROM php:7.3-fpm

ENV DEBIAN_FRONTEND noninteractive

#RUN apt-get update \
#    && apt-get install -y --no-install-recommends locales apt-utils git;

RUN apt-get update -y && \
    apt-get install -y --no-install-recommends git unzip
#
#RUN echo "en_US.UTF-8 UTF-8" > /etc/locale.gen && \
#    echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen && \
#    locale-gen
#
#COPY php.ini /usr/local/etc/php/php.ini
#
#RUN curl -sSk https://getcomposer.org/installer | php -- --disable-tls && \
#   mv composer.phar /usr/local/bin/composer

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /app