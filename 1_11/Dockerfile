FROM amazoncorretto:8-jdk

EXPOSE 8080

WORKDIR /usr/src/app

COPY . .

RUN chmod+x ./mvnw package

CMD [ "java", "-jar", "./target/docker-example-1.1.3.jar" ]