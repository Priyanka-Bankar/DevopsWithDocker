# Exercise 
# 1.1. Getting started

## Instructions

Since we already did "Hello, World!" in the material let's do something else.

Start 3 containers from an image that does not automatically exit (such as nginx) in detached mode.

Stop two of the containers and leave one container running.

As an answer write the output for docker ps -a which shows 2 stopped containers and one running.

## Start three containers in detached mode

```shell
docker run -d nginx 
docker run -d redis
docker run -d mysql
```
## check container name
``` shell 
docker container ls
```
## Output
```shell
CONTAINER ID      IMAGE         COMMAND                  CREATED         STATUS                         PORTS           NAMES
feb8a549388b      httpd     "httpd-foreground"       7 seconds ago      Up 6 seconds                    80/tcp       upbeat_wing
6b2a9d5f8cab      redis     "docker-entrypoint.s…"   18 minutes ago     Up 18 minutes                   6379/tcp     priceless_napier
1fb4ca85782f      nginx     "/docker-entrypoint.…"   19 minutes ago     Up 19 minutes                   80/tcp       nice_shockley
```

## Stopping two containers
```shell
docker stop upbeat_wing
docker stop priceless_napier
```
## Output
```shell
docker ps -a
CONTAINER ID   IMAGE        COMMAND                  CREATED          STATUS                      PORTS             NAMES
feb8a549388b   httpd     "httpd-foreground"       5 minutes ago    Exited (0) 17 seconds ago                    upbeat_wing
6b2a9d5f8cab   redis     "docker-entrypoint.s…"   34 minutes ago   Exited (0) 5 seconds ago                     priceless_napier
1fb4ca85782f   nginx     "/docker-entrypoint.…"   34 minutes ago   Up 34 minutes                  80/tcp        nice_shockley