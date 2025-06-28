# Exercise
# 1.4. Missing dependencies
## Instructions

Start a Ubuntu image with the process running the following script ``sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'``

If you're on Windows, you'll want to switch the ' and " around: ``sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://$website; done"``.

The small script uses the command line tool curl to load url of a website and prints that to screen. If you try the script, it does not work

```
Input website:
helsinki.fi
Searching..
sh: 1: curl: not found
```
Your task is to fix the error by installing curl inside the container.

You are done with the exercise when the response looks something like this

```
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.24.0</center>
</body>
</html>
```
Hint for installing the missing dependencies you could start a new process with ``docker exec``. And remember: google is your friend on using Ubuntu.


As the answer, write the command you used to start the process and the command(s) you used to fix the ensuing problems.

## command tp start process
```
~ docker run -it --name looper ubuntu sh -c "while true; do echo 'Input website:'; read website; echo 'Searching..'; sleep 1; curl http://\$website; done" 
```
## command to fix problem
```
~ docker exec -it looper bash
root@67512b8613af:/# apt update
root@67512b8613af:/# apt install curl -y
```
