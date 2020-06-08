# Section Two

* Define a container with Dockerfile
* Build and test your image
* Run your image as a container

## Terminal 

kellyblackledge@Kellys-MBP dockerorientationhw % git clone https://github.com/dockersamples/node-bulletin-board
cd node-bulletin-board/bulletin-board-app
Cloning into 'node-bulletin-board'...
remote: Enumerating objects: 124, done.
remote: Total 124 (delta 0), reused 0 (delta 0), pack-reused 124
Receiving objects: 100% (124/124), 185.01 KiB | 942.00 KiB/s, done.
Resolving deltas: 100% (54/54), done.
kellyblackledge@Kellys-MBP bulletin-board-app % docker build --tag bulletinboard:1.0
"docker build" requires exactly 1 argument.
See 'docker build --help'.

Usage:  docker build [OPTIONS] PATH | URL | -

Build an image from a Dockerfile
kellyblackledge@Kellys-MBP bulletin-board-app % docker build --tag bulletinboard:1.0 .
Sending build context to Docker daemon  45.57kB
Step 1/7 : FROM node:current-slim
current-slim: Pulling from library/node
e62d08fa1eb1: Pull complete 
faf966cc3d43: Pull complete 
e6d70bb71fcf: Pull complete 
e875b66c84cb: Pull complete 
1e999b3ce618: Pull complete 
Digest: sha256:338cdfe7fba3a9f1c8edc3452fa7213398bb86a09969a9bf2ab79fcdf7acdc4f
Status: Downloaded newer image for node:current-slim
 ---> 26379995b148
Step 2/7 : WORKDIR /usr/src/app
 ---> Running in c8e9bef5951b
Removing intermediate container c8e9bef5951b
 ---> be9df3391266
Step 3/7 : COPY package.json .
 ---> 3fd6aef5682d
Step 4/7 : RUN npm install
 ---> Running in 538d27e03e1e

> ejs@2.7.4 postinstall /usr/src/app/node_modules/ejs
> node ./postinstall.js

Thank you for installing EJS: built with the Jake JavaScript build tool (https://jakejs.com/)

npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN vue-event-bulletin@1.0.0 No repository field.
npm WARN The package morgan is included as both a dev and production dependency.

added 91 packages from 168 contributors and audited 92 packages in 7.765s
found 0 vulnerabilities

Removing intermediate container 538d27e03e1e
 ---> 1f2de926b16e
Step 5/7 : EXPOSE 8080
 ---> Running in 4fe6c0295983
Removing intermediate container 4fe6c0295983
 ---> efb4d367bbeb
Step 6/7 : CMD [ "npm", "start" ]
 ---> Running in 663810d52eea
Removing intermediate container 663810d52eea
 ---> 6b93582b9933
Step 7/7 : COPY . .
 ---> 1a9238a00e87
Successfully built 1a9238a00e87
Successfully tagged bulletinboard:1.0
kellyblackledge@Kellys-MBP bulletin-board-app % docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0
c6d3fce50ca27699da83be6dc37f142fffb8dfc1f4fcaa7797f317e1473620f2
kellyblackledge@Kellys-MBP bulletin-board-app % docker rm --force bb
bb
