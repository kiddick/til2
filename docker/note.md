### list images
`docker images`

### list containers
`docker ps -a`

### create container (interactive run)
`docker run -it --name image-from-container ubuntu:14.04`

### create image from container (hard to reproduce)
`docker commit image-from-container myimage`

### cahge entrypoint
`docker commit  --change "ENTRYPOINT /usr/bin/python3" create-image-from-me`

### Dockerfile
```
 # source image
FROM ubuntu:14.04

# info about maintainer
LABEL maintainer="S Y" 

ENTRYPOINT ["bin/sh"]
```

### build docker contaier from file (care about content of source dir)
`docker build -t image-from-dockerfile .`

https://docs.docker.com/engine/reference/builder/

https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

### layered fs
![](2019-01-16-15-29-41.png)

### mount file to container
```
docker run -it -rm -v $(pwd):/home ubuntu:14.04
```
