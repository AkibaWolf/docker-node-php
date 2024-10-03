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
    php8.3 \
    php8.3-apcu \
    php8.3-cli \
    php8.3-common \
    php8.3-curl \
    php8.3-intl \
    php8.3-mbstring \
    php8.3-memcached \
    php8.3-mysql \
    php8.3-opcache \
    php8.3-xml \
    php8.3-xsl \
    php8.3-zip
