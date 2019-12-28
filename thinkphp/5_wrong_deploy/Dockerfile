FROM composer
MAINTAINER Dem0ns <www@yangblog.cn>
RUN composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/ && \
    cd /srv && composer create-project topthink/think www "5.1.*"
CMD cd /srv/www/ && php -S 0.0.0.0:8000
EXPOSE 8000
