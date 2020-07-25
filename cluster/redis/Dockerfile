FROM redis:latest

ARG REDIS_PORT

COPY redis.conf /etc/redis/redis.conf

RUN sed -i 's/REDIS_PORT/'$REDIS_PORT'/g' /etc/redis/redis.conf

ENTRYPOINT redis-server /etc/redis/redis.conf