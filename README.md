# Docker-Q-A

1)Docker?
A)Docker is a containerization tool or Docker is a software to create  container by using the docker image.we can create 'n' no of containers on a host operating system and all containers are virtually seperated. (or)
Docker is a software/computer program that performs operating system level virtualization,also known as containerization.

2)Containerization?
A)Containerizatio is a process of packaging an application along with it's required libraries,frameworks and configuration files together so that it can be run in various environments efficiently.


Docker commands:
systemctl status docker -->To know the status of the docker(whether it is running or not)
docker --version ->to know the docker version
docker version  ->if you want to see client as well as docker server informantion we use docker version
docker info ->to get more information about your docker

Docker image commads:
docker images(it will give the list of images)
docker image ls  (which will show how many images are in our local system.)
docker rmi <imageid> (to remove the image)
docker image -q(it will give you the imageid) 

docker search (serivice name) 
example:docker search tomcat
docker pull (service name) :it will the pull the image rom docker hub. 
example: docker pull tomcat

Docker container commands:
dockert create imageid   (To create container by using " dockerimage")
docker run -it -d sericename(service name example ubuntu or centos or tomcat or etc)
docker ps (it will only show running containers.)
docker ps -a/ --all (it will show all the running as well as stopped containers)
docker exec -it <container id> bash (to enter into a  running container as bash)
docker exec -it <container id> sh   ((to enter into a  running container as shell))
 *after entered into that conatiner if you want to verify what type of OS it is just run cmd: cat /etc/os-release
 *to comeout ctrl +press p and q (both for shell and bash)
docker start containerid (to start the container)
docker stop containerid(to stop the cotainer)
docker rm -f containerid (to remove the single contailer)(-f means forcefully)(we can't jst remove a container while running)
docker rm  containerid (to remove container after stoping the container)
docker run -it -d --name vishnu imagename (to assain a custom name to a container)
docker rename container_oldname conatiner_newname ( rename to a container)
docker stats (it will show the memory usage by the container)(after ontainer start)
docker system df(it will give you the all the  disk usage by the images and conainers,etc..)
docker system prune(this will remove all the stopped containers,all networks not used by atleast one containers,all dangling images & all bild cache)
Note:dangling images means the images which are not associated with the containers)
docker system prune -a(it will remove all the images,this will remove all the stopped containers,all networks not used by atleast one containers,
all dangling images & all bild cache)
  
Summary:

BASIC:
docker version
docker -v
docker info
docker --help
docker login

images:
docker images
docker pull
docker rmi

containers:
docker ps
docker run
docker start
docker stop

system:
docker stats
docker system df
docker system prune
