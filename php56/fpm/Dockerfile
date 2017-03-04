################################################################################
# Base image
################################################################################

FROM php:5.6-fpm

################################################################################
# Build instructions
################################################################################

# Install packages
RUN apt-get update && apt-get install -y \
    libmcrypt-dev \
    libicu-dev \
    libxslt-dev \
  && docker-php-ext-install -j$(nproc) \
    intl \
    mcrypt \
    xsl \
    sockets \
    bcmath \
    pcntl \
    opcache
  
RUN apt-get install -y \
    libevent-dev \
  && pecl install ev-1.0.3 xdebug-2.5.1 \
  && docker-php-ext-enable ev
