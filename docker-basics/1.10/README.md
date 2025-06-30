# Exercise
# 1.10. Ports open
## Instructions
The image devopsdockeruh/simple-web-service will start a web service in port 8080 when given the argument "server". In Exercise 1.8 you already did an image that can be used to run the web service without any argument.

Use now the -p flag to access the contents with your browser in http://localhost:8080. The output to your browser should be something like: `` { message: "You connected to the following path: ..." }``

Give command(s) used to start the service

## Dockerfile
```
FROM devopsdockeruh/simple-web-service:alpine

EXPOSE 8080

CMD ["server"]
```
## commands
```
docker build -t simple-web-server .
docker run -p 8080:8080 simple-web-server
```
## output
```
{
  "message": "You connected to the following path: /",
  "path": "/"
}
```