FROM node:17

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
    && wget -q https://packages.sury.org/php/apt.gpg -O- | apt-key add - \
    && echo "deb https://packages.sury.org/php/ bullseye main" | tee /etc/apt/sources.list.d/php.list \
    \
    && echo "### Update packages" \
    \
    && apt-get -y update \
    && apt-get -y upgrade \
    \
    && echo "### Install required PHP packages" \
    \
    && apt-get -y install \
        php8.1 \
        php8.1-cli \
        php8.1-common \
        php8.1-curl \
        php8.1-intl \
        php8.1-mbstring \
        php8.1-memcached \
        php8.1-mysql \
        php8.1-opcache \
        php8.1-xml \
        php8.1-zip
