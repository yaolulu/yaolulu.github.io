## Docker

### Step 1: Install Docker

1. First, in order to ensure the downloads are valid, add the GPG key for the official Docker repository to your system.

		curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

2. Add the Docker repository to APT sources
		
		sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable


3. update the package database with the Docker packages from the newly added repo
		
		sudo apt-get update

4. Make sure you are about to install from the Docker repo instead of the default Ubuntu 16.04 repo

		apt-cache policy docker-ce

5. Install Docker

		sudo apt-get install -y docker-ce

6. Check Docker status

		sudo systemctl status docker

The output should be similiar to the following. 

		Output
		● docker.service - Docker Application Container Engine
   		Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
   		Active: active (running) since Thu 2018-10-18 20:28:23 UTC; 35s ago
     		Docs: https://docs.docker.com
 		Main PID: 13412 (dockerd)
   			CGroup: /system.slice/docker.service
           			├─13412 /usr/bin/dockerd -H fd://
           			└─13421 docker-containerd --config /var/run/docker/containerd/containerd.toml


## Step 2: Executing the Docker Command Without Sudo (Optional)

		sudo usermod -aG docker ${USER}

		su - ${USER}

		id -nG

## Step 3: Working With Docker Images

Docker containers are run from Docker images. By default, it pulls these images from Docker Hub, a Docker registry managed by Docker, the company behind the Docker project. Anybody can build and host their Docker images on Docker Hub, so most applications and Linux distributions you'll need to run Docker containers have images that are hosted on Docker Hub.

Let's take Unubtu for examplle.

1. Search for images
		
		docker search ubuntu

2. In the OFFICIAL column, OK indicates an image built and supported by the company behind the project. Once you've identified the image that you would like to use, you can download it to your computer using the pull subcommand.

		docker pull ubuntu

3. After an image has been downloaded, you may then run a container using the downloaded image with the run subcommand. If an image has not been downloaded when docker is executed with the run subcommand, the Docker client will first download the image, then run a container using it.

		docker run ubuntu

4. To see the images that have been downloaded to your computer, type:

		docker images


## Step 4: Running a Docker Container

		docker run -it ubuntu

		docker run -it --rm --network host -v <project_path>:/ptab/ -w=/ptab -e PYTHONPATH=/ptab/ <image name>  /bin/bash

