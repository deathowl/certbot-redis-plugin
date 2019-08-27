# Certbot-Redis
Certbot plugin for Redis
![travis](https://travis-ci.org/deathowl/certbot-redis-plugin.svg?branch=master "Build status")




Installation guide:
* Install [Redis](https://redis.io/)
* Deploy latest version of [Certbot](https://github.com/certbot/certbot)
* Install certbot-redis `plugin pip install certbot-redis`

## Use cases:
* Get/Renew and install new certificate


 ``` certbot certonly -a certbot-redis:redis --certbot-redis:redis-redis-url=your_redis_server:port```

* Keep in mind, that you'll need a webapplication, that reads the challenge from redis, and responds to it at .well-known/acme-challenge/{key}
