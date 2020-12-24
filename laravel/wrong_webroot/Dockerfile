FROM composer
RUN composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/ && \
    composer global require laravel/installer && \
    cd /srv && \
    composer create-project --prefer-dist laravel/laravel www "5.8.*"
CMD cd /srv/www && php -S 0.0.0.0:8000
EXPOSE 8000
