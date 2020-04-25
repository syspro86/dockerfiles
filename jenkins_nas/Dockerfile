FROM jenkins/jenkins:latest

USER root
RUN apt-get update && apt-get -y install build-essential sudo

RUN apt-get install -y apt-transport-https ca-certificates curl software-properties-common
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
RUN apt-get update && apt-get install -y pkg-config libssl-dev libsasl2-dev libcurl4-openssl-dev docker-ce

RUN echo "jenkins ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers

USER jenkins

EXPOSE 8080
