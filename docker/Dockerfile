FROM php:7.3-apache

# node, yarn
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash && \
    set -x && . ~/.bashrc && \
    nvm install v12.4.0 && \
    curl -o- -L https://yarnpkg.com/install.sh | bash

EXPOSE 80
