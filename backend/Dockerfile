FROM php:8.1-apache

# Install required dependencies
RUN apt-get update && \
    apt-get install -y libpng-dev && \
    apt-get install -y unzip && \
    apt-get install -y wget

WORKDIR /var/www/html

COPY . .

RUN docker-php-ext-install pdo_mysql && \
    docker-php-ext-install gd

CMD bash -c "sleep 5 && php artisan migrate:fresh --seed && php artisan passport:client --personal & sleep 5 && php artisan serve --host=0.0.0.0"
