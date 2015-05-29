FROM sample/apache-php:prod

ADD . /srv/application

RUN cd /srv/application && composer update && composer install -n
RUN rm -rf /var/www
RUN ln -s /srv/application/public /var/www
RUN chown -R www-data:www-data /srv/application