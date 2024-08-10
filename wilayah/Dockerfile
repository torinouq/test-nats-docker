FROM torinouq/ci-core:dev-8.1.27-phpfpm
# php:7.3.6-fpm base

WORKDIR /var/www/html

# COPY ./src /var/www/html/src
COPY conf/php.ini "$PHP_INI_DIR/"
COPY conf/www.conf /usr/local/etc/php-fpm.d/

RUN chown www-data:www-data -R /var/www/html \
    && chmod -R 777 /var/www/html

EXPOSE 9000

CMD [ "php-fpm" ]