# Exercise
# 1.3. Secret message
## Instructions
Now that we've warmed up it's time to get inside a container while it's running!

Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the running container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".

What are the commands to see the secret message

## commands

```
~ docker run  devopsdockeruh/simple-web-service:ubuntu 
~ docker exec -it charming_tu  bash
~ tail -f ./text.log
```
What is the secret message

## secret message
```
Secret message is: 'You can find the source code here: https://github.com/docker-hy' 2025-06-24 14:59:34 +0000 UTC 2025-06-24 14:59:36 +0000 UTC 2025-06-24 14:59:39 +0000 UTC 2025-06-24 14:59:41 +0000 UTC 2025-06-24 14:59:43 +0000 UTC Secret message is: 'You can find the source code here: https://github.com/docker-hy' 2025-06-24 14:59:45 +0000 UTC 2025-06-24 14:59:47 +0000 UTC 2025-06-24 14:59:49 +0000 UTC 2025-06-24 14:59:51 +0000 UTC 2025-06-24 14:59:53 +0000 UTC Secret message is: 'You can find the source code here: https://github.com/docker-
```