FROM alpine:3.9

ADD https://dl.bintray.com/php-alpine/key/php-alpine.rsa.pub /etc/apk/keys/php-alpine.rsa.pub

RUN apk --update add ca-certificates

RUN echo "https://dl.bintray.com/php-alpine/v3.9/php-7.3" >> /etc/apk/repositories

RUN apk update \
	&& apk add --update \
	    curl \
		php \
		php-common \
		php-bcmath \
		php-curl \
		php-dom \
		php-exif \
		php-gd \
		php-gettext \
		php-gmp \
		php-iconv \
		php-intl \
		php-json \
		php-ldap \
		php-mbstring \
		php-mysqli \
		php-opcache \
		php-openssl \
		php-pdo \
		php-pdo_mysql \
		php-pdo_sqlite \
		php-sqlite3 \
		php-xml \
		php-zip \
		php-zlib \
		php-phar \
		php-memcached \
		php-mongodb \
		php-xdebug

RUN ln -s /usr/bin/php7 /usr/bin/php
