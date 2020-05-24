FROM node:10

# Modify package sources
COPY etc/apt/sources.list /etc/apt/sources.list

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
    && echo "deb https://packages.sury.org/php/ stretch main" | tee /etc/apt/sources.list.d/php.list \
    \
    && echo "### Update packages" \
    \
    && apt-get -y update \
    && apt-get -y upgrade \
    \
    && echo "### Install required PHP packages" \
    \
    && apt-get -y install \
        php7.4 \
        php7.4-cli \
        php7.4-common \
        php7.4-curl \
        php7.4-intl \
        php7.4-mbstring \
        php7.4-memcached \
        php7.4-mysql \
        php7.4-opcache \
        php7.4-xml \
        php7.4-zip
