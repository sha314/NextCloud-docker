# NextCloud-docker
using docker-compose to set up nextcloud

# Install docker
## Fedora
sudo dnf -y install dnf-plugins-core

sudo dnf config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo
    
sudo dnf install docker-ce docker-ce-cli containerd.io




## AlmaLinux
sudo yum-config-manager --add-repo  https://download.docker.com/linux/rhel/docker-ce.repo    

#sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   
sudo dnf -y install docker-ce docker-ce-cli containerd.io


# Start and check
sudo systemctl start docker
sudo docker run hello-world

# enable during startup
sudo systemctl enable docker

# Install docker-compose

sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version


# Install NextCloud

