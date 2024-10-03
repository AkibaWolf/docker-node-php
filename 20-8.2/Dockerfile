FROM node:20-bookworm AS os-base

# Install base packages
RUN apt update -y
RUN apt upgrade -y
RUN apt install -y --no-install-recommends \
    apt-transport-https \
    ca-certificates \
    curl \
    git \
    mc \
    nano \
    vim \
    unzip \
    wget \
    zip

# Add PHP repositories
RUN wget -q https://ftp.mpi-inf.mpg.de/mirrors/linux/mirror/deb.sury.org/repositories/php/apt.gpg -O- | apt-key add - 
RUN echo "deb https://packages.sury.org/php/ bookworm main" | tee /etc/apt/sources.list.d/php.list

# Update packages
RUN apt update -y

# --------------------------------------------------------------------------------------

FROM os-base AS php-base

# Install required PHP packages
RUN apt install -y --no-install-recommends \
    php8.2 \
    php8.2-apcu \
    php8.2-cli \
    php8.2-common \
    php8.2-curl \
    php8.2-intl \
    php8.2-mbstring \
    php8.2-memcached \
    php8.2-mysql \
    php8.2-opcache \
    php8.2-xml \
    php8.2-xsl \
    php8.2-zip
