FROM        docker.io/redhat/ubi9 AS builder
RUN         dnf install maven -y
RUN         mkdir /app
ADD         https://github.com/roboshop-devops-project-v3/shipping.git /app
WORKDIR     /app
RUN         mvn clean package
ENTRYPOINT  ["java", "-jar", "/app/target/shipping-1.0.jar"]

#FROM        docker.io/redhat/ubi9
#RUN         dnf install java-17-openjdk -y

FROM        docker.io/openjdk:17-ea-17-slim
COPY        --from=builder /app/target/shipping-1.0.jar /shipping-1.0.jar
ENTRYPOINT  ["java", "-jar", "/shipping-1.0.jar"]

