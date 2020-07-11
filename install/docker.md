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

# ADMINISTRAÇÃO
 docker ps <!-- Lista os containers criados -->
 docker ps -a <!-- Lista todos os containers -->
 docker images <!--Lista as imagens baixadas -->
 docker run <!-- Realiza a execução de um container -->
 docker run -ti hello-world <!-- t (terminal), i (interação), hello-world (imagem) -->
 docker container attach <!-- Acessar container em execução -->
