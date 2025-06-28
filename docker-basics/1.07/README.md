# Exercise
# 1.7. Image for script
## Instructions

We can improve our previous solutions now that we know how to create and build a Dockerfile.

Let us now get back to Exercise 1.4.

Create a new file script.sh on your local machine with the following contents:

```
#!/bin/bash
while true
do
  echo "Input website:"
  read website; echo "Searching.."
  sleep 1; curl http://$website
done
``` 

Create a Dockerfile for a new image that starts from ubuntu:24.04 and add instructions to install curl into that image. Then add instructions to copy the script file into that image and finally set it to run on container start using CMD.

After you have filled the Dockerfile, build the image with the name "curler".

If you are getting permission denied, use chmod to give permission to run the script.

The following should now work:

```
$ docker run -it curler

  Input website:
  helsinki.fi
  Searching..
  <!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
  <html><head>
  <title>301 Moved Permanently</title>
  </head><body>
  <h1>Moved Permanently</h1>
  <p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
  </body></html>

```
Give your Dockerfile as answer.

## output
```
# Start from the Ubuntu image

FROM ubuntu:24.04 

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.

WORKDIR /usr/src/app

# Copy the script.sh file from this location to /usr/src/app/ creating /usr/src/app/script.sh.

COPY script.sh .

# Execute a command with `/bin/sh -c` prefix.

RUN apt update && apt install -y curl

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.

RUN chmod +x script.sh

# When running Docker run the command will be ./hello.sh

CMD ["./script.sh"]
