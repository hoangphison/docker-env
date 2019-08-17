FROM hoangphison/php:5.6-cli-alpine

LABEL maintainer="hello@hoangphison.com"

ENV COMPOSER_HOME /root/composer

ENV COMPOSER_VERSION master

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN apk add --update --no-cache \
        git \
        unzip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && composer global require hirak/prestissimo

VOLUME ["/app"]

WORKDIR /app

CMD ["-"]

ENTRYPOINT ["composer", "--ansi"]
