FROM codercom/code-server

USER root

# java 11
RUN apt-get update && apt-get install -y openjdk-11-jdk maven

# python 3.6
RUN apt-get update && apt-get install -y python3 python3-pip
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3.6 1
RUN update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 1

ADD .profile /home/coder/

USER coder
