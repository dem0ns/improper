FROM php:7.1.3-fpm
COPY --from=composer /usr/bin/composer /usr/bin/composer
RUN sed -i "s/\w*.debian.org/mirrors.aliyun.com/g" /etc/apt/sources.list
RUN apt-get update 2>&1 ; apt-get install -y \
    zlib1g-dev \
    libzip-dev
RUN docker-php-source extract \
    && docker-php-ext-install zip \
    && docker-php-source delete
WORKDIR /var/www/html/
RUN composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/ \
    && composer global require laravel/installer \
    && composer create-project --prefer-dist laravel/laravel laravel "5.8.*"
RUN chown -R www-data:www-data laravel
