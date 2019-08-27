FROM php:7.3-alpine

LABEL maintainer="hello@hoangphison.com"

ENV PHPCS_VERSION=3.4.2

RUN curl -L https://github.com/squizlabs/PHP_CodeSniffer/releases/download/$PHPCS_VERSION/phpcs.phar > /usr/local/bin/phpcs \
    && chmod +x /usr/local/bin/phpcs \
    && rm -rf /var/cache/apk/* /var/tmp/* /tmp/*

VOLUME ["/app"]

WORKDIR /app

ENTRYPOINT ["phpcs"]

CMD ["--version"]