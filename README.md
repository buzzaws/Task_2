# Task 2: Dockerize a Sample Application

## Objective: Containerize a simple web application using Docker.

#### Steps:

####  install docker on ubuntu 

#### Command to install docker :

#### Update the package index
sudo apt-get update

## Install necessary packages
sudo apt-get install ca-certificates curl

#### Create the directory for apt keyrings with correct permissions
sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

#### Add the Docker repository to apt sources
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

#### Update the package index again
sudo apt-get update

#### Install Docker packages
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

