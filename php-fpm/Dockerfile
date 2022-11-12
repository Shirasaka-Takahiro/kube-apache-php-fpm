FROM php:7.4.26-fpm
RUN mkdir -p /usr/local/apache2/sites-enabled/hoge.com/public_html \
    && touch /usr/local/apache2/sites-enabled/hoge.com/public_html/phpinfo.php
COPY ./phpinfo.php /usr/local/apache2/sites-enabled/hoge.com/public_html/phpinfo.php
EXPOSE 9000