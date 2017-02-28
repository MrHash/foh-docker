################################################################################
# Base image
################################################################################

FROM php:5.6-cli

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
    json \
    iconv \
    mcrypt \
    xsl \
    sockets \
    bcmath
  
RUN apt-get install -y \
    libevent-dev \
  && pecl install ev-1.0.3 \
  && docker-php-ext-enable ev
