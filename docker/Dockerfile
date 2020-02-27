FROM romeoz/docker-nginx-php:7.2

RUN apt-get update \
    && apt-get -y install git vim \
    # install composer
    && curl -s https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin/ --filename=composer \
    && apt-get autoremove -y \
    && apt-get clean -y

RUN rm -rf /etc/nginx/conf.d/*
COPY app.conf /etc/nginx/sites-enabled/app.conf

EXPOSE 80