FROM php:5.6
MAINTAINER Dem0ns <www@yangblog.cn>
RUN cd /tmp/ && \
    curl -L -O https://github.com/top-think/thinkphp/archive/v3.2.5.tar.gz && \
    mkdir /srv/www && tar xf v3.2.5.tar.gz && rm -f v3.2.5.tar.gz && \
    mv thinkphp-3.2.5/* /srv/www/ && rm -rf thinkphp-3.2.5
CMD cd /srv/www/ && php -S 0.0.0.0:8000
EXPOSE 8000
