FROM redis:latest

COPY redis.conf /etc/redis/redis.conf

ENTRYPOINT sed -i 's/REDIS_PORT/'$REDIS_PORT'/g' /etc/redis/redis.conf \
&& redis-server /etc/redis/redis.conf
