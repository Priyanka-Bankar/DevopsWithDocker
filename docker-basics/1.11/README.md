# Exercise
# 1.11. Spring
## Instructions
Create a Dockerfile for an old Java Spring project that can be found from the course repository(opens in a new tab).

The setup should be straightforward with the README instructions. Tips to get you started:

There are many options for running Java, you may use eg. amazoncorretto(opens in a new tab) FROM amazoncorretto:_tag_ to get Java instead of installing it manually. Pick the tag by using the README and Docker Hub page.

You've completed the exercise when you see a 'Success' message in your browser.

Submit the Dockerfile and the command you used to run the container.

## commands for clonning repository and copy spring-example project to folder 1.11

```
git clone https://github.com/docker-hy/material-applications
cp -r spring-example-project ../docker-basics/1.11/
touch Dockerfile
```

## commands to build and run 
```
docker build . -t myapp1.11
docker run -p 8080:8080 myapp1.11
```