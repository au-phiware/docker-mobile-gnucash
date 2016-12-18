FROM php:7-fpm-alpine
RUN docker-php-ext-install pdo pdo_mysql
ADD https://raw.githubusercontent.com/justinhunt1223/mobilegnucash/master/index.php /usr/src/
RUN chmod a+r /usr/src/index.php
