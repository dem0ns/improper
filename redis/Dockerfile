FROM ubuntu
RUN sed -i 's/\w*.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
RUN apt update && \
    apt install redis -y && \
    apt install openssh-server -y
RUN sed -i 's/^bind 127.0.0.1 ::1$/bind 0.0.0.0/g' /etc/redis/redis.conf
RUN sed -i 's/^daemonize yes$/daemonize no/g' /etc/redis/redis.conf
RUN mkdir /root/.ssh
CMD service ssh start && redis-server /etc/redis/redis.conf
EXPOSE 6379
EXPOSE 22
