FROM hub.c.163.com/library/php:7.0.23-fpm
ADD php.ini /usr/local/etc/php/php.ini
ADD sources.list /etc/apt/sources.list  
ADD so/phpredis-3.1.4 /var/www/so/phpredis-3.1.4
WORKDIR /var/www/so/phpredis-3.1.4
RUN phpize && ./configure && make && make install
RUN docker-php-ext-enable redis