# Section One

* Download and install Docker Desktop
* Test Docker version
* Test Docker Installation

## Terminal
kellyblackledge@Kellys-MBP dockerorientationhw % docker --version
Docker version 19.03.8, build afacb8b
kellyblackledge@Kellys-MBP dockerorientationhw % docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

kellyblackledge@Kellys-MBP dockerorientationhw % run docker image ls
zsh: command not found: run
kellyblackledge@Kellys-MBP dockerorientationhw % docker image ls
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
dockercomposehw_web         latest              772a1bf84669        23 hours ago        227MB
python-barcode              latest              2a3d8b293ac8        23 hours ago        958MB
kb8njit/docker101tutorial   latest              f6220e69a280        25 hours ago        26.5MB
docker101tutorial           latest              f6220e69a280        25 hours ago        26.5MB
<none>                      <none>              08fa5707061d        25 hours ago        121MB
<none>                      <none>              e240cbf55544        25 hours ago        220MB
<none>                      <none>              8e9b67263361        25 hours ago        108MB
redis                       alpine              e008f2ff99d0        4 days ago          31.5MB
python                      3.7-alpine          6a5ca85ed89b        5 days ago          72.5MB
python                      alpine              8ecf5a48c789        5 days ago          78.9MB
node                        12-alpine           1c342643aa5c        5 days ago          89.4MB
nginx                       alpine              7d0cdcc60a96        6 days ago          21.3MB
python                      3                   659f826fabf4        2 weeks ago         934MB
hello-world                 latest              bf756fb1ae65        5 months ago        13.3kB
kellyblackledge@Kellys-MBP dockerorientationhw % docker ps
CONTAINER ID        IMAGE                 COMMAND                  CREATED             STATUS              PORTS                    NAMES
86e2e0dbe751        dockercomposehw_web   "flask run"              23 hours ago        Up 23 hours         0.0.0.0:5000->5000/tcp   dockercomposehw_web_1
d2a45b0b882d        redis:alpine          "docker-entrypoint.s…"   23 hours ago        Up 23 hours         6379/tcp                 dockercomposehw_redis_1
22cc3ad95d5f        docker101tutorial     "/docker-entrypoint.…"   25 hours ago        Up 25 hours         0.0.0.0:80->80/tcp       docker-tutorial
