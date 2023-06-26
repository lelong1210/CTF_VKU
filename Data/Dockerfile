FROM orsolin/docker-php-5.3-apache
COPY ./src /var/www/html/

RUN a2enmod rewrite
RUN service apache2 restart

EXPOSE 80