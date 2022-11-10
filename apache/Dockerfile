FROM httpd:2.4
RUN mkdir -p /usr/local/apache2/sites-enabled/hoge.com/public_html \
    && touch /usr/local/apache2/sites-enabled/hoge.com/public_html/index.html \
    && touch /usr/local/apache2/sites-enabled/hoge.com/public_html/phpinfo.php \
    && touch /usr/local/apache2/conf/extra/hoge.com.conf \
    && touch /usr/local/apache2/conf/extra/proxy-php.conf
COPY ./httpd.conf /usr/local/apache2/conf/httpd.conf
COPY ./proxy-php.conf /usr/local/apache2/conf/extra/proxy-php.conf
COPY ./hoge.com/hoge.com.conf /usr/local/apache2/conf/extra/hoge.com.conf
COPY ./hoge.com/index.html /usr/local/apache2/sites-enabled/hoge.com/public_html/index.html
COPY ./hoge.com/phpinfo.php /usr/local/apache2/sites-enabled/hoge.com/public_html/phpinfo.php
WORKDIR /usr/local/apache2/sites-enabled/hoge.com/public_html
EXPOSE 80