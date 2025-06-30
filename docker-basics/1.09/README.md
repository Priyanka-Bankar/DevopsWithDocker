# Exercise
# 1.9. Volumes
## Instructions
Image devopsdockeruh/simple-web-service creates a timestamp every two seconds to /usr/src/app/text.log when it's not given a command. Start the container with a bind mount so that the logs are created into your filesystem.

Hint: read the note that was made just before this exercise!

As the answer submit the command(s) you used to complete the exercise.

## commands
```
touch text.log
docker run -v"$(pwd)/text.log:/usr/src/app/text.log" devopsdockeruh/simple-web-service
```
