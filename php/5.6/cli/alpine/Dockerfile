FROM alpine:3.8

LABEL maintainer="hello@hoangphison.com"

RUN apk add --update --no-cache \
    ca-certificates \
    curl \
    php5 \
    php5-zip \
    php5-mysqli \
    php5-pdo \
    php5-pdo_mysql \
    php5-pdo_sqlite \
    php5-sqlite3 \
    php5-mcrypt \
    php5-exif \
    php5-gd \
    php5-xml \
    php5-curl \
    php5-json \
    php5-openssl \
    php5-phar \
    php5-dom \
    php5-opcache \
    php5-zlib \
    php5-ldap

RUN ln -s /usr/bin/php5 /usr/bin/php

CMD ["php", "-a"]
