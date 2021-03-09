# INSTALAÇÃO
- sudo apt-get install -y docker-ce docker-ce-cli containerd.io
- docker -v
- curl -L https://github.com/docker/machine/releases/download/v0.16.1/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine
- docker-machine -v

# CONFIGURAÇÃO

# DESINSTALAÇÃO
- dpkg -l | grep -i docker <!-- Verificação de instalações -->
- sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
- sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce
- sudo rm -rf /var/lib/docker /etc/docker
- sudo groupdel docker
- sudo rm -rf /var/run/docker.sock

# ADMINISTRAÇÃO
- docker ps <!-- Lista os containers criados -->
- docker ps -a <!-- Lista todos os containers -->
- docker images <!--Lista as imagens baixadas -->
- docker run <!-- Realiza a execução de um container -->
- docker run -ti ubuntu <!-- t (terminal), i (interação), ubuntu (imagem) -->
- docker run -d nginx <!-- Realizar a execução de um container em modo daemon -->
- docker run -d -m 128M --cpus 1 nginx <!-- Delimitando a quantidade de Memoria e CPU para o container -->
- docker rub -ti --mount type=bind,src=fonte,dst=destino ubuntu <!-- Montagem de um apontamento para o local aonde ficara os dados -->
- docker run -ti --mount type=volume,src=nome_do_volume,dst=destino ubuntu <!-- Montagem de um volume para o local aonde ficara os dados -->
- docker run -p 8080:80 <!-- Expõe a porta 8080 para conectar na 80 do container -->
- docker run -P <!-- Expõe qualquer porta aliatória -->
- docker volume create nome <!-- Criação de um volume -->
- docker volume ls <!-- Lista os volumes -->
- docker attach <!-- Acessar container em execução -->
- docker exec -it youthful_wiles bash <!-- Executar alguma ação dentro do container -->
- docker stop <!-- Para o container -->
- docker start <!-- Inicia o container -->
- docker restart <!-- Reinicia o container -->
- docker pause <!-- Realiza o pause do container -->
- docke unpause <!-- Retorna o container a sua execução -->
- docker inspect <!-- Verificar as informações do container -->
- docker logs <!-- Verifica os logs do container -->
- docker rm <!-- Remover containers -->
- docker stats <!-- Verificar o status do container -->
- docker top <!-- Verificar os processos que estão sendo executados dentro do container -->
- docker update <!-- Realiza a atualização de um container em execução -->
- docker image build -t name:version . <!-- Realização do build -->
- docker system prune -a <!-- Remove todos os recursos associados ao docker -->
- docker container prune <!-- Remove todos os containers -->
- docker volume prune <!-- Remove todos os volumes -->
- docker commit <!-- Realiza a criação de uma imagem apartir de um container -->
- docker image tag <!-- Adiciona tags a uma imagem de container -->
- docker push <!-- Sobe a image gerada para o DockerHub -->
- docker pull <!-- Realizar o download da imagem -->
- docker-machine version
- docker-machine create --driver virtualbox linuxtips
- docker-machine ls
- docker-machine env linuxtips
- eval "$(docker-machine env linuxtips)"
- docker container ls
- docker container run busybox echo "LINUXTIPS, VAIIII"
- docker-machine ip linuxtips
- docker-machine ssh linuxtips
- docker-machine inspect linuxtips
- docker-machine stop linuxtips
- docker-machine ls 
- docker-machine start linuxtips
- docker-machine rm linuxtips
- eval $(docker-machine env -u)
