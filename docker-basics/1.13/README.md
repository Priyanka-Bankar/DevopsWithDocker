# Exercise
# 1.13. Hello backend (mandatory exercise)
## Instructions

Clone, fork or download a project from https://github.com/docker-hy/material-applications/tree/main/example-backend(opens in a new tab).

Create a Dockerfile for the project (example-backend). Start the container with port 8080 published.

When you start the container and navigate to http://localhost:8080/ping(opens in a new tab) you should get a "pong" as a response.

Do not alter the code of the project

TIPS:

depending on your base image, you might need this(opens in a new tab)
If you have M1/M2 Mac, you might need to build the image with an extra option docker build --platform linux/amd64 -t imagename .

Submit the Dockerfile and the commands used as the answer.


## command to build and run
```
docker build . -t backend-example
docker run -p 8080:8080 backend-example
```