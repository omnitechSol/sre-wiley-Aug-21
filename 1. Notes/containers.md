### ##########################
### Site Reliability Engineering [Container_Notes]
### ##########################


### Keywords
- SDDC (Software Defined Data Center)
      - Server Virtualization (Hypervisors)
      - Storage Virtualization (SAN)
      - Network Virtualization (SDN)


### Container Runtimes
- Docker
- CRI-O
- Rkt
- Containerd
- Podman


### Container Orchestration Engines (COE)
- Kubernetes
- Apache Meso
- Docker Swarm
- EKS
- ECS
- AKS
- GKE

### Docker Architecture
- Docker host
- Docker Daemon
- Docker client
- Docker images
- Docker containers
- Docker registry (Within a registry there will be multiple repositories)
      - Public (hub.docker.com) --> GitHub for your images
      - Private (AWS ECR)


### Analogy for Docker

Dockerfile ~= Vagrantfile ~= CloudFormation ~= Terraform ~= Vrealize templates
Docker images ~= Vagrant Box ~= Amazon AMI ~= VMware Templates
Docker containers ~= Virtual Machines ~= Amazon EC2 ~= VMware VMs


### Class Activity 1
````
1. Install docker
2. create a user docker-admin (make sure to use command "adduser" and not "useradd")
3. usermod -aG docker docker-admin (Run this command as root)
4. Search image for nginx using docker search or by going to hub.docker.com
5. Pull the image to your docker host
6. Run a container from this newly pulled image

````

### Class Activity 2
````
1. Download nginx or ubuntu image
2. Create a container from the image
3. go into the container and make some changes (like creating a user or file etc.)
4. Come out of the container and commit changes to a new image
5. Make sure your image name is compliant with Docker recommended nomenclature
6. Push your newly created image to your DockerHub
7. Verify the changes on DockerHub.
````

### Docker commands
````
docker search keyword
docker images (docker image ls) --> List all images on Docker host
docker pull nginx --> pull nginx image from Docker hub to you local Docker host
docker ps (docker container ls) --> List all running containers
docker ps -a (docker container ls -a) --> List all running/stopped containers
docker run -it <imagename>
    -i - interactive
    -t - terminal/tty
    -d - detached / daemonized

-it --> root user mode
-itd --> detached mode


docker stop container_id
docker start container_id
docker attach container_id (equivalent of SSH in VMs)

exit --> exit the container and stop
ctrl+P+Q --> exit the container without stopping

docker rm (docker container rm) --> delete a container
docker rmi (docker image rm) --> delete an image from docker host


````

nginx ---> nginx:latest
hello-world --> hello-world:latest
ubuntu --> ubuntu:latest ---> 

docker pull ubuntu:xenial
docker pull ubuntu:bionic


docker pull myapp:v1
docker pull myapp:v2
docker pull myapp:v3


sk12k/imagename


sk12k-nginx --> sk12k/mynewnginx



created user sk12k
created file /tmp/info.txt
Installed package "tree"








### References
- https://docs.docker.com/get-started/overview/
- https://get.docker.com/
- https://hub.docker.com/
- 



