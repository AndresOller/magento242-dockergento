# build ontop of the PHP 7.4 image
FROM modestcoders/php:7.4-fpm

USER root

# add ini files in a path relative to this Dockerfile
COPY ./conf/php.ini /usr/local/etc/php/

USER app:app
