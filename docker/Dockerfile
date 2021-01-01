

FROM ubuntu:latest
WORKDIR /deb

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -q -y \
build-essential debhelper dpkg-dev apt-utils gnupg scons libao-dev libspeechd-dev 

COPY src /src
COPY package *.key *.pub ./
RUN ./package
CMD [ "cat", "rhvoice.tar" ]
