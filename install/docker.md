# INSTALAÇÃO
 sudo apt-get install -y docker-ce docker-ce-cli containerd.io
 docker version

# DESINSTALAÇÃO
 dpkg -l | grep -i docker
 sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
 sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce
 sudo rm -rf /var/lib/docker /etc/docker
 sudo groupdel docker
 sudo rm -rf /var/run/docker.sock