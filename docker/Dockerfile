FROM php:7.3-apache

# mysql-client and php extensions
RUN apt-get update && \
    apt-get install --no-install-recommends -y mysql-client && \
    docker-php-ext-install pdo_mysql mysqli mbstring

# allow htaccess
RUN a2enmod rewrite

# composer
RUN apt-get install --no-install-recommends -y zip && \
    curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer && \
    chmod +x /usr/local/bin/composer

# node, yarn
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash && \
    set -x && . ~/.bashrc && \
	nvm install stable && \
	curl -o- -L https://yarnpkg.com/install.sh | bash

EXPOSE 80
