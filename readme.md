## Setup

All source code should be in app folder

- rename core.example.yaml to docker.yaml 
- rename web.example.yaml to web.yaml 
- rename env.example to .env
- create folder app in the core of project

### Run docker

create new network with name which you set in .env param DEFAULT_NETWORK

```sh
 docker network create docker NAME
```
Then run main config

```sh
 docker-compose -f core.yaml up -d
```

Then run web config

```sh
 docker-compose -f web.yaml up -d
```

Attach information about your host in local machine (hosts file)

```sh
 127.0.0.1 name (which you set in .env param WEB)
```

### Includes

 
| Plugin | README |
| ------ | ------ |
| Traefik | [Readme](https://hub.docker.com/_/traefik) |
| Nginx | [Readme](https://hub.docker.com/_/nginx)  |
| Mysql | [Readme](https://hub.docker.com/_/mysql)  |
| Phpmyadmin | [Readme](https://hub.docker.com/r/phpmyadmin/phpmyadmin)  |
| Php-fpm | [Readme](https://hub.docker.com/r/nanoninja/php-fpm)  |