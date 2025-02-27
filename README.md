# Task 2: Dockerize a Sample Application

## Objective: Containerize a simple web application using Docker.

#### Steps:
 
i)install docker on ubuntu 

##Command to install docker##

sudo apt update

sudo apt install docker.io -y

####### start the docker service #######

sudo systemctl start docker

sudo systemctl enable docker

sudo systemctl status docker


<img width="1200" alt="Screenshot 2025-02-27 at 11 38 56 PM" src="https://github.com/user-attachments/assets/e1d9c586-8f56-4fbc-a327-f1a70a2e5a85" />


######################    Create Simple Python Application   #####################

i) Install python and package manager pip

ii) Install flask using pip

iii) create simple flask App

iv)  create requirements.txt

#######################   Create Docker file  ####################################

i) Create dockerfile

ii) Build Image 

command to build image

docker build -t flask-docker-app .

iii) Run the container using build Image

Command to run the docker container

docker run -d flask-docker-app:latest

iv) Access via web browser

34.230.4.107:8000


<img width="1200" alt="Screenshot 2025-02-27 at 11 51 59 PM" src="https://github.com/user-attachments/assets/25496201-17da-43de-aa4a-23e756a7fdd2" />


<img width="1200" alt="Screenshot 2025-02-27 at 11 51 08 PM" src="https://github.com/user-attachments/assets/d0d0eee3-72ca-4d36-907c-05994f9402a8" />

############  Push the Docker image to Docker Hub or AWS Elastic Container Registry (ECR).  ###########

docker tag flask-docker-app:latest buzzeraws/assignment:latest

docker login -u buzzeraws -p buzzeraws

docker push buzzeraws/assignment:latest

<img width="1200" alt="Screenshot 2025-02-28 at 12 50 30 AM" src="https://github.com/user-attachments/assets/3aaac33c-c538-4bcb-b7e0-a47c5e4fbfaf" />




