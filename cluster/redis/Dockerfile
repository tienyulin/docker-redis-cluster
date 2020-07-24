FROM redis:latest

EXPOSE $REDIS_PORT

COPY redis.conf /etc/redis/redis.conf

ENTRYPOINT redis-server /etc/redis/redis.conf
