################################################################################
# Base image
################################################################################

FROM php:7.1.2-fpm

################################################################################
# Build instructions
################################################################################

# Install packages
RUN apt-get update && apt-get install -y \
    libmcrypt-dev \
    libicu-dev \
    libxslt-dev \
    libzmq3-dev \
    libevent-dev \
  && docker-php-ext-install -j$(nproc) \
    intl \
    mcrypt \
    xsl \
    sockets \
    bcmath \
    pcntl \
    opcache

RUN apt-get install -y \
  && pecl install ev-1.0.3 xdebug-2.5.1 \
  && docker-php-ext-enable ev \
  && pecl install zmq-1.1.3 \
  && docker-php-ext-enable zmq
