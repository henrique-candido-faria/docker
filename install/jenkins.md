docker network create jenkins

docker volume create jenkins
docker volume ls | grep jenkins
docker volume inspect jenkins

docker container run --name jenkins -d --restart=always -p 8080:8080 -p 50000:50000 -u 0 -v jenkins:/var/jenkins_home --network jenkins jenkins:latest

docker container exec "id_do_container" cat /var/jenkins_home/secrets/initialAdminPassword