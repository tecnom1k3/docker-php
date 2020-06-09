FROM php:7.4-fpm-alpine

RUN apk add --no-cache \
    git

RUN echo "UTC" > /etc/timezone

ENV COMPOSER_HOME /composer
ENV PATH ./vendor/bin:/composer/vendor/bin:$PATH
ENV COMPOSER_ALLOW_SUPERUSER 1
#RUN curl -s https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer