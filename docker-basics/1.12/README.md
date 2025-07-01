# Exercise
# 1.12. Hello frontend (mandatory exercise)
## Instructions
A good developer creates well-written READMEs. Such that they can be used to create Dockerfiles with ease.

Clone, fork or download the project from https://github.com/docker-hy/material-applications/tree/main/example-frontend(opens in a new tab).

Create a Dockerfile for the project (example-frontend) and give a command so that the project runs in a Docker container with port 5000 exposed and published so when you start the container and navigate to http://localhost:5000 you will see a message if you're successful.
``
note that the port 5000 is reserved in the more recent OSX versions, so you have to use some other host port
``
As in other exercises, do not alter the code of the project

TIPS:

The project has install instructions in README.
Note that the app starts to accept connections when "Accepting connections at http://localhost:5000" has been printed to the screen, this takes a few seconds
You do not have to install anything new outside containers.
The project might not work with too new Node.js versions

Give the Dockerfile and the commands you used for building and running the image as the answer.

## commands to move folder to our project folder
```
mv ~/git/DevopsWithDocker/material-applications/example-frontend .
```
# command to build and run 
```
docker build . -t reactapp
docker run -p 5000:5000 myapp1.12
```