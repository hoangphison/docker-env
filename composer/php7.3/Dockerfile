FROM hoangphison/php:7.3-cli

ENV COMPOSER_HOME /root/composer

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN apk add --update --no-cache --virtual .persistent-deps \
    curl \
    git \
    unzip \
    php-phar

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && composer global require hirak/prestissimo \
    && composer global clear-cache

VOLUME ["/app"]

WORKDIR /app

CMD ["-"]

ENTRYPOINT ["composer", "--ansi"]