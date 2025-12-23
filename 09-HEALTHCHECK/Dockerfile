FROM        docker.io/redhat/ubi9
RUN         dnf install nginx -y
ENTRYPOINT  ["nginx", "-g", "daemon off;"]
EXPOSE      80
HEALTHCHECK --interval=5s --timeout=3s CMD curl -f http://localhost/dummy

