
FROM ubuntu:latest
WORKDIR /deb

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -q -y \
curl gnupg

COPY rhvoice-deb-test ./
RUN ./rhvoice-deb-test
