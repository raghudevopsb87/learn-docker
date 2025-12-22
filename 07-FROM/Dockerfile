FROM        docker.io/redhat/ubi9
RUN         dnf install maven -y
RUN         mkdir /app
ADD         https://github.com/roboshop-devops-project-v3/shipping.git /app
WORKDIR     /app
RUN         mvn clean package
ENTRYPOINT  ["java", "-jar", "/app/target/shipping-1.0.jar"]

