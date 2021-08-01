## DOCKER COMMANDS ##

### Docker Client Image Commands
## docker version
docker version
docker info

## docker commands help page
docker pull --help
docker build --help

### Docker Client Container Commands
## docker pull
docker pull [image name]
docker pull mkodockx/docker-clamav:alpine

## docker build Build the image using:
docker build . ltkvien/sftponazure
docker build -t ltkvien/sftponazure
docker build -t [your_image_name] .

## docker images
docker images
docker images [image name]

## The follwing two commands will tag and push the container to ACR.
docker tag {iamge_id} {image_new_name}:{tag} 
docker tag hello-world deploy.azurecr.io/hello-world
docker tag nginx ltkvien.azurecr.io/samples/nginx
docker tag docker-clamav:alpine ltkvien.azurecr.io/clamav
docker tag docker-clamav:alpine ltkvien.azurecr.io/clamav
docker tag sftp:alpine ltkvien.azurecr.io/sftp
docker tag 553296eba4cc ltkvien/sftponazure
docker tag 425d9581f8ba  p1docker-clamav:alpine

## docker run # Run the image using:
# docker run
docker run --name {container_name} -p {host_port}:{container_port} -v {/host_path}:{/container_path} -it {image_name} /bin/bash
docker run -p 8080:5000 -v $(pwd):/app [image_name]
docker run [image name]
# docker run interactive mode
docker run --interactive --tty ubuntu bash
docker run -it --rm -p 3310:3310 mkodockx/docker-clamav:alpine
docker run -it -p 3310:3310 ltkvien.azurecr.io/docker-clamav:alpine
docker run [image_name] -it bash
# docker run 
docker run -d -p 3310:3310 ltkvien.azurecr.io/docker-clamav:alpine 
# docker run with mount volume
docker run --volume /volume_name [image_name] bash

## docker login
docker login docker.io
docker login ltkvien.azurecr.io

## docker ps
docker ps
docker ps -a

## docker push
docker push ltkvien.azurecr.io/hello-world
docker push ltkvien.azurecr.io/samples/nginx
docker push ltkvien.azurecr.io/clamav
docker push ltkvien/sftponazure

# docker pull
docker pull mkodockx/docker-clamav:alpine
docker pull docker-clamav:alpine ltkvien.azurecr.io
docker pull ltkvien/sftp:alpine

## docker start
docker start {new_container_name}

## docker stop
docker stop [container_id]

## docker exec
docker exec -it 1b45c549c3c1 /bin/bash
docker exec -it docker-clamav /bin/bash
docker exec -it <container_name> bash

## docker commit
docker commit -m "message" {container_name} {image_name}

## docker remove
# docker remove container
docker rm [container ID]
docker rm <list_container_name_or_id>
# docker remove image
docker rmi [image ID]
docker rmi {425d9581f8ba/p1docker-clamav }

## docker rename
docker rename
docker rename gallant_carson docker-clamav

## docker save
docker save ltkvien.azurecr.io/docker-clamav:alpine > {D:/docker-clamav.tar}

## docker import
cat musashi.tar | docker import - {new_image_name}:latest

## docker detach # If you'd like to run in detached mode add -d to the docker run command
docker -d #--detach, -d.

## docker history
docker history {image_name}

## docker log
docker logs --follow your_name_container

### docker-compose Commands
## docker-compose version
docker-compose --version

## docker-compose build
docker-compose build

### Docker Machine Commands

docker-machine start [machine name]
docker-machine stop [machine name]
docker-machine env [machine name]
docker-machine ip [machine name]
docker-machine status [machine name]





