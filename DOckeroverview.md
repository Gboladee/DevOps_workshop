Docker
Docker is a containerization technology and it is a platform that is focused on creating and running containers. Other containerization technologies include

LXC
Hyper-V and windows containers
rkt
podman, amidst others.
TERMS IN DOCKER
The docker architecture consists of various terminologies that are important to know.

Docker client — The docker client is also knows as the Docker Command Line Interface or CLI. Running a docker command starts up the docker client. The CLI will take the command, process it, and communicate with the docker server.
Docker Machine — Docker Machine is a tool that lets you install Docker Engine on virtual hosts, and manage the hosts with docker-machine commands.
Docker Image — A docker image is a file containing all the dependencies and configuration required to run a specific program.
Docker Hub — Docker hub is a repository used for finding and sharing container images.
BASIC DOCKER COMMANDS
Docker run {Insert image name} — This is used to create and run images.
Docker ps — This gives information about the containers running on docker. This includes The container ID, when they were created, e.t.c. However, it only shows containers that are running at that time.
Docker ps — — all — This shows all the containers that have ever been run on docker.
Docker create { insert Docker command}— This returns as the ID of the container
Docker start -a {Container ID} — To start the previously created container
NOTE : It is worthy of note that Docker run consists of 2 commands, Docker create and Docker start.

Other Commands
Restart container — docker start -a container ID
Remove stopped containers — docker system prune
Debug docker containers — docker logs container ID
Stop a container — Docker stop container ID or Docker kill container ID
To start up a shell — docker run -it imagename sh
To exit a container — Cntrl + C, Cntrl +D, or Exit.
Create a Docker Image
To create a Docker Image, we need to create a docker file. A docker file is a plain text file that contains configurations. This contains our programs content.

Creating a Docker file

Specify a base Image
Run some commands to install additional programs
Specify a command to run on Container start up.
Building a Docker file

Create a directory.
Change into the directory
Start up your code editor within this directory
Use an existing docker image as a base eg FROM alpine (A base image is basically an Operating system for the container)
Download and Install dependencies E.g RUN apk add — — update redis
Tell the image what to do when it starts eg CMD [“Redis-server”]
After creating your docker file, type docker build within your terminal. If it worked, you should get the following message as a return message “successfully build” followed by 12 characters.
Insert Docker run followed by the characters it returned
In conclusion, this article can be likened to a glance over the world of docker. This topic can never be exhausted as it is so broad however, having a strong foundation by grasping the basics is pertinent in mastering this tool.
