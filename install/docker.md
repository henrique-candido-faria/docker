# INSTALAÇÃO
 curl -fsSL https://get.docker.com | bash
 docker version

# DESINSTALAÇÃO
 dpkg -l | grep -i docker
 sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
 sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce
 sudo rm -rf /var/lib/docker /etc/docker
 sudo rm /etc/apparmor.d/docker
 sudo groupdel docker
 sudo rm -rf /var/run/docker.sock