FROM redis:latest

ARG REDIS_PORT

EXPOSE $REDIS_PORT

COPY sentinel.conf /etc/redis/sentinel/sentinel.conf

RUN sed -i 's/REDIS_PORT/'$REDIS_PORT'/g' /etc/redis/sentinel/sentinel.conf

ENTRYPOINT redis-sentinel /etc/redis/sentinel/sentinel.conf
