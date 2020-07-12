# INSTALAÇÃO
- sudo apt-get install -y docker-ce docker-ce-cli containerd.io
- docker version

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
- docker attach <!-- Acessar container em execução -->
- docker exec <!-- Executar alguma ação dentro do container -->
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