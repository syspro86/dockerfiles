FROM codercom/code-server

USER root

# java 11
RUN apt-get update && apt-get install -y openjdk-11-jdk maven

# python 3.6
RUN apt-get update && apt-get install -y python3
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3.6 1

USER coder
