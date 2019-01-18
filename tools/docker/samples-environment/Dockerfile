# Docker file to create an environment for building/testing samples.
#
# To build new image use
#   docker build -t docker-registry.labs.intellij.net/kotlin-native/samples-environment:1 .
#
# To publish image to the JB internal registry use
#   docker push docker-registry.labs.intellij.net/kotlin-native/samples-environment:1

FROM ubuntu

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get -y install sudo default-jdk libgit2-dev libgtk-3-dev freeglut3-dev libsdl1.2-dev

RUN apt-get -y install python-pip python-dev build-essential
RUN pip install --upgrade pip
RUN pip install --upgrade virtualenv
RUN pip -q install typing

RUN rm -rf /var/lib/apt/lists/*
