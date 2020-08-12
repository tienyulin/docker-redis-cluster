# Redis
![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/tienyu/redis-cluster)

## How To Use
```bash=
docker run --name redis-cluster-node --net=host -e REDIS_PORT=<port> -p <port>:<port> -v <volume path>:/data tienyu/redis-cluster
```
