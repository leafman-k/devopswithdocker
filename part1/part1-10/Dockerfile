FROM ubuntu:16.04

WORKDIR /frontend

COPY ./dist ./dist
RUN apt-get update
RUN apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs
RUN node -v
RUN npm -v
RUN npm install -g serve

ENTRYPOINT ["serve","-s", "-l", "5000", "dist"]
