# Exercise
# 1.2 Cleanup
Stop all your containers.


Now you have containers and some images that are no longer in use and are taking up space. Running docker ps -a and docker image ls will confirm this.

Clean the Docker daemon by removing all images and containers.

As an answer give the output for docker ps -a and docker image ls


```shell
docker ps -a

CONTAINER ID   IMAGE        COMMAND                  CREATED          STATUS                      PORTS         NAMES
feb8a549388b   httpd     "httpd-foreground"       5 minutes ago    Exited (0) 17 seconds ago                upbeat_wing
592eba56a2a6   mysql     "docker-entrypoint.s…"   32 minutes ago   Exited (1) 14 minutes ago                brave_sammet
6b2a9d5f8cab   redis     "docker-entrypoint.s…"   34 minutes ago   Exited (0) 5 seconds ago                 priceless_napier
1fb4ca85782f   nginx     "/docker-entrypoint.…"   34 minutes ago   Exited (0) 14 minutes ago                80/tcp      nice_shockley
```
## Removeing all containers
```shell
docker container rm upbeat_wing
docker container rm brave summit
docker container rm priceless_napier
docker container rm nice_shockley
```
## Output
```
docker container ls -a

CONTAINER ID   IMAGE        COMMAND                  CREATED          STATUS                      PORTS         NAMES

```

## Removing all images
```
docker image rm httpd
docker image rm mysql
docker image rm redis
docker image rm nginx
```
## Output
```
docker image ls -a

CONTAINER ID   IMAGE        COMMAND                  CREATED          STATUS                      PORTS         NAMES
````