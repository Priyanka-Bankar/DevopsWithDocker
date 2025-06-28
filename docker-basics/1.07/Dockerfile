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

