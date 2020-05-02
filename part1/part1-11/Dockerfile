FROM ubuntu:16.04

WORKDIR /backend

COPY ./backend-example-docker-master .
RUN apt-get update
RUN apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs
RUN node -v
RUN npm -v
RUN npm install

ENTRYPOINT ["npm","start"]
