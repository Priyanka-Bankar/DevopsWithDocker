# Exercise 

# 1.5. Sizes of images

Instructions

In the Exercise 1.3 we used devopsdockeruh/simple-web-service:ubuntu.

Here is the same application but instead of Ubuntu is using Alpine Linux(opens in a new tab): devopsdockeruh/simple-web-service:alpine.

Pull both images and compare the image sizes.

Go inside the Alpine container and make sure the secret message functionality is the same. Alpine version doesn't have bash but it has sh, a more bare-bones shell.

What is the size of the alpine image (in MB):

```
devopsdockeruh/simple-web-service   alpine        dd4d367476f8   4 years ago    24.3MB
```

What is the size of the ubuntu image (in MB):

```
devopsdockeruh/simple-web-service   ubuntu        d44e1dce3987   4 years ago    126MB
```

# Checking secret  message in alpine container

## Run alpine container
```
docker run -d -it devopsdockeruh/simple-web-service:alpine    
```
## check container name
```
docker container ps -a
```
## output
```
CONTAINER ID   IMAGE                                        COMMAND                   CREATED          STATUS         PORTS     NAMES
638b24f9258f   devopsdockeruh/simple-web-service:alpine    "/usr/src/app/server"     7 seconds ago     Up 6 seconds           modest_swanson
```
## enter inside container and output message
```
 docker exec -it modest_swanson sh

 /usr/src/app # tail -f ./text.log

 ```

 ## output
 ```
 2025-06-27 14:41:08 +0000 UTC
2025-06-27 14:41:10 +0000 UTC
2025-06-27 14:41:12 +0000 UTC
2025-06-27 14:41:14 +0000 UTC
2025-06-27 14:41:16 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2025-06-27 14:41:18 +0000 UTC
2025-06-27 14:41:20 +0000 UTC
2025-06-27 14:41:22 +0000 UTC
2025-06-27 14:41:24 +0000 UTC
2025-06-27 14:41:26 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2025-06-27 14:41:28 +0000 UTC
2025-06-27 14:41:30 +0000 UTC
2025-06-27 14:41:32 +0000 UTC
2025-06-27 14:41:34 +0000 UTC
```

