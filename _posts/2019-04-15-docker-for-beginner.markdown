## Docker

### Step1 : Install Docker

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