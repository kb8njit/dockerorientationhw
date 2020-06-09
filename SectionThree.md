# Section Three

* Set up your Docker Hub account
* Create a Docker Hub repository and push your image

## Terminal

kellyblackledge@Kellys-MBP dockerorientationhw % docker login
Authenticating with existing credentials...
Login Succeeded
kellyblackledge@Kellys-MBP dockerorientationhw % cd node-bulletin-board/bulletin-board-app
kellyblackledge@Kellys-MBP bulletin-board-app % docker tag bulletinboard:1.0 kb8njit            
kellyblackledge@Kellys-MBP bulletin-board-app % docker push kb8njit/bulletinboard:1.0

The push refers to repository [docker.io/kb8njit/bulletinboard]
An image does not exist locally with the tag: kb8njit/bulletinboard
kellyblackledge@Kellys-MBP bulletin-board-app % docker tag bulletinboard:1.0 <Your Docker ID>/bulletinboard:1.0
zsh: no such file or directory: Your
kellyblackledge@Kellys-MBP bulletin-board-app % docker tag bulletinboard:1.0 kb8njit/bulletinboard:1.0
kellyblackledge@Kellys-MBP bulletin-board-app % docker push kb8njit/bulletinboard:1.0
The push refers to repository [docker.io/kb8njit/bulletinboard]
0bf3cb53e8ae: Pushed 
495437230fc8: Pushed 
8ac6df748fe3: Pushed 
f2249cfbc597: Pushed 
cbbf68640dde: Mounted from library/node 
d7f5c170793c: Mounted from library/node 
63afc1153abd: Mounted from library/node 
daee265ea6cb: Mounted from library/node 
83b43189420d: Mounted from library/node 
1.0: digest: sha256:74418c3f1b1bab8ffcf63361d6341701d2bfd6be0a44451d5f3c9704b83a2d04 size: 2201
