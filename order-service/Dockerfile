#Base Image
FROM openjdk:8-jre-alpine

MAINTAINER  everythingisdata.githib.io 

COPY . /var/converter
WORKDIR /var/converter


#To Reduce Tomcat startup time. We added a system property pointing to "dev/urandom" as source of entropy.
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","target/order-service-0.0.1-SNAPSHOT.jar"]

#On port application will listing
EXPOSE 8300 8787