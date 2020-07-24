FROM redis:latest

EXPOSE $REDIS_PORT

COPY ./sentinel.conf /etc/redis/sentinel/sentinel.conf

ENTRYPOINT redis-sentinel /etc/redis/sentinel/sentinel.conf
