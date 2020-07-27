FROM redis:latest

COPY sentinel.conf /etc/redis/sentinel/sentinel.conf

ENTRYPOINT sed -i 's/REDIS_PORT/'$REDIS_PORT'/g' /etc/redis/sentinel/sentinel.conf \
&& redis-sentinel /etc/redis/sentinel/sentinel.conf
