
FROM debian:latest
WORKDIR /deb

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -q -y \
curl gnupg locales locales-all

ENV LC_ALL ru_RU.UTF-8
ENV LANG ru_RU.UTF-8
ENV LANGUAGE ru_RU.UTF-8

COPY rhvoice-deb-test ./
RUN ./rhvoice-deb-test
CMD [ "cat", "test.wav" ]
