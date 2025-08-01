# Exercise
# 1.8. Two line Dockerfile
## Instructions
By default our `devopsdockeruh/simple-web-service:alpine` doesn't have a CMD. Instead, it uses *ENTRYPOINT* to declare which application is run.

We'll talk more about *ENTRYPOINT* in the next section, but you already know that the last argument in docker run can be used to give a command or an argument.

As you might've noticed it doesn't start the web service even though the name is "simple-web-service". A suitable argument is needed to start the `server`!

Try docker run `devopsdockeruh/simple-web-service:alpine hello`. The application reads the argument "hello" but will inform that hello isn't accepted.

In this exercise create a Dockerfile and use FROM and CMD to create a brand new image that automatically runs server.

The Docker documentation CMD(opens in a new tab) says a bit indirectly that if a image has ENTRYPOINT defined, CMD is used to define it the default arguments.

Tag the new image as "web-server"

Running the built "web-server" image should look like this:

```
$ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
- using env:   export GIN_MODE=release
- using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```
We don't have any method of accessing the web service yet. As such confirming that the console output is the same will suffice.
The exercise title may be a useful hint here.

If you are a M1 MAC user you will get the following warning that can be ignored for now

`WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested`

Answer with the Dockerfile and the command you used to run the container.

## Dockerfile
```
FROM devopsdockeruh/simple-web-service:alpine

CMD ["server"]
```

## Output
```
~ docker build -t web-server .
~ docker run web-server
```
