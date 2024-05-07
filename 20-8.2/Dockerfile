FROM node:20-bookworm

# Set up environment, build & install required packages
RUN echo "### Add PHP repositories" \
    \
    && apt-get -y update \
    && apt-get -y install \
        apt-transport-https \
        ca-certificates \
        curl \
        git \
        mc \
        nano \
        vim \
        wget \
    && wget -q https://ftp.mpi-inf.mpg.de/mirrors/linux/mirror/deb.sury.org/repositories/php/apt.gpg -O- | apt-key add - \
    && echo "deb https://packages.sury.org/php/ bookworm main" | tee /etc/apt/sources.list.d/php.list \
    \
    && echo "### Update packages" \
    \
    && apt-get -y update \
    && apt-get -y upgrade \
    \
    && echo "### Install required PHP packages" \
    \
    && apt-get -y install \
        php8.2 \
        php8.2-cli \
        php8.2-common \
        php8.2-curl \
        php8.2-intl \
        php8.2-mbstring \
        php8.2-memcached \
        php8.2-mysql \
        php8.2-opcache \
        php8.2-xml \
        php8.2-zip
