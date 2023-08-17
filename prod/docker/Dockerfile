FROM php:7.4-fpm
WORKDIR /var/www/html
COPY . /var/www/html
RUN apt-get update && apt-get install -y \
    # Add any necessary extensions here
    && docker-php-ext-install mysqli pdo pdo_mysql \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
EXPOSE 9000

CMD ["php-fpm"]

