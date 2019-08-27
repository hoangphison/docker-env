FROM hoangphison/php:7.3-cli-alpine

LABEL maintainer="hello@hoangphison.com"

ENV COMPOSER_HOME /root/composer

ENV COMPOSER_VERSION "1.9.0"

ENV COMPOSER_ALLOW_SUPERUSER 1

ENV COMPOSER_MEMORY_LIMIT -1

RUN apk add --update --no-cache \
        git \
        unzip

RUN curl -sS https://getcomposer.org/installer | php -- \
        --install-dir=/usr/local/bin \
        --filename=composer \
        --version=${COMPOSER_VERSION} \
    && composer global require hirak/prestissimo

VOLUME ["/app"]

WORKDIR /app

CMD ["-"]

ENTRYPOINT ["composer", "--ansi"]
