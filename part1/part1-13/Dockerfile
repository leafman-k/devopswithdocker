FROM openjdk:8

WORKDIR /spring

COPY ./spring-example-project-master .
RUN apt-get update && apt-get -y install maven
RUN ./mvnw package

ENTRYPOINT java -jar ./target/docker-example-1.1.3.jar
