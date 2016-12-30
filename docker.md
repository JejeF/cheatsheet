# Docker


## Setup
* install docker (see the links in the reference)
* add User to the docker group: `sudo usermod -aG docker $USER`


## Basic command
* `docker run 'image_name'`
* `docker ps -a` show all the contener
* `docker images`
* `docker build -t 'image_name'`
* `docker tag 'image_id' 'tag-name'/'image_name':lastest'`
* `docker rmi -f 'image_id'`


* `docker run 'name'`
* `docker start 'name'`
* `docker stop 'name''`


* `docker logs -f 'name'`
* `docker top 'name'`
* `docker inspect 'name'`

## Exemple
* `mkdir project`
* `touch Dockerfile` macke a dorcker file with this content:
```dockerfile
FROM docker/whalesay:latest
RUN apt-get -y update && apt-get install -y fortunes
CMD /usr/games/fortune -a | cowsay
```
* `docker build -t docker-whale .` build
* `docker images` see the new images
* `docker run docker-whale` run the contener with the image


## Reference
https://docs.docker.com/engine/installation/linux/ubuntulinux/

https://docs.docker.com/engine/getstarted/
