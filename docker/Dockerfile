FROM php:8.2-alpine
WORKDIR /var/www
COPY composer.json /var/www/composer.json
COPY phpcpd /var/www/phpcpd
COPY tools/composer /var/www/tools/composer
COPY src /var/www/src
RUN /var/www/tools/composer install
ENTRYPOINT ["/var/www/phpcpd","${@}"]