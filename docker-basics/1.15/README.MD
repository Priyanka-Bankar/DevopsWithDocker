# Exercise
# 1.15. Homework
## Instructions
Create Dockerfile for an application or any other dockerised project in any of your own and publish it to Docker Hub. This can be any project, except the clones or forks of backend-example or frontend-example.

Make sure you at least have a basic description and instructions for how to run the application in the Repository overview of the project Docker Hub page.

For the answer provide the link to the project in Docker Hub in the form username/repository.

## Answer

Link : https://hub.docker.com/r/priyanka57/hello-python

## commands to publish on docker hub

```
touch Dockerfile
touch hello.py
docker build -t your-dockerhub-username/hello-python .
docker run your-dockerhub-username/hello-python
docker login
docker push your-dockerhub-username/hello-python

```