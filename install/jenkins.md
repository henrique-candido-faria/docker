docker volume create jenkins_home
docker volume ls | grep jenkins_home
docker volume inspect jenkins_home

docker container run --name jenkins -d --restart=always -p 8080:8080 -p 50000:50000 -u 0 -v jenkins_home:/var/jenkins_home jenkins