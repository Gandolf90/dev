FROM phpdockerio/php80-fpm:latest

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install php8.0-mysql php8.0-intl php8.0-mbstring php8.0-sqlite3 sendmail nano php-redis\
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

WORKDIR "/var/www/"

RUN chown -R www-data:www-data "/var/www/"
RUN chmod -R 0755 "/var/www/"

ENV REDIS_HOST="redis"
ENV REDIS_PASS="redis"