FROM lavoweb/php-5.6
MAINTAINER lavoweb <aurelien@lavoweb.net>

RUN docker-php-ext-enable opcache
RUN echo '\nopcache.enable_cli=1 \n\
opcache.memory_consumption=512 \n\
opcache.max_accelerated_files=100000 \n\
opcache.validate_timestamps=0 \n\
opcache.consistency_checks=0'>> /usr/local/etc/php/conf.d/docker-php-ext-opcache.ini


COPY b2b/b2b.servais.ephec-ti.be.conf /etc/apache2/site-enabled/
COPY www/servais.ephec-ti.be.conf /etc/apache2/site-enabled/
COPY www/index.html /var/www/html/site1
COPY b2b/index.php /var/www/html/site2


EXPOSE 80
VOLUME /app


