# Docker Steps

docker images

docker run alpine 
docker run nginx:alpine
docker run alpine sleep 10

docker exec cont cat /etc/hosts

docker ps

docker ps -a

docker stop

docker rm 

docker rmi alpine

docker pull

docker run -dit alpine sleep 10

docker run -d -p 80:80 my_image service nginx start

docker exec -it agitated_lewin /bin/bash

docker inspect 

git clone https://github.com/arunksingh16/docker.git

docker build . -t arun161087/microservice:v1

docker run -p 8080:8080 -dit arun161087/microservice:v1

docker logs

docker push arun161087/microservice:v1

docker run -dit --name aks -p 8090:80 -v /home/scrapbook/tutorial/:/usr/local/apache2/htdocs/ httpd:2.4

docker run -p 80:80 -dit --name aks arun161087/docker-http-server

docker run ubuntu cat /etc/hosts

docker run -it ubuntu bash 


===============================================================================================================

docker build -t webserver-image:v1 .


docker run -d -p 80:80 webserver-image:v1
