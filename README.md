# jenkins

docker run -p 8000:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock -v jenkins_home:/var/jenkins_home --name jenkinsjon juananmora/jenkins:latest


version: '3'

services:
  jenkins:
    image: jenkins/jenkins:latest
    ports:
      - "8001:8080"
    volumes:
      - /home/qatools/volumes/jenkins_home:/var/jenkins_home
      - /var/run/docker.sock:/var/run/docker.sock
