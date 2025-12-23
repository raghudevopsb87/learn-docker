FROM        docker.io/redhat/ubi9
LABEL       Project="RoboShop Inc"
RUN         dnf install nginx -y
ENTRYPOINT  ["nginx", "-g", "daemon off;"]
EXPOSE      80
ONBUILD     RUN rm -rf /usr/share/nginx/html/*

