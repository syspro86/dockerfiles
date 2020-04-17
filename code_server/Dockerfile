FROM codercom/code-server

USER root

# docker
RUN apt-get update && apt-get -y install apt-transport-https ca-certificates curl software-properties-common gnupg2
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

RUN sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"

RUN apt-get update && apt-get -y install pkg-config libssl-dev libsasl2-dev libcurl4-openssl-dev docker-ce

# java 11
RUN apt-get install -y openjdk-11-jdk maven

# python 3.6
RUN apt-get install -y python3 python3-pip
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3.7 1
RUN update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 1

# profile (git credentials)
ADD .profile /home/coder/

USER coder
