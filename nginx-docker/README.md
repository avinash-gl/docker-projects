
# 🌐 NGINX Docker Static Website

A simple project that demonstrates how to serve a static website using **NGINX** inside a **Docker container**.

## 🐳 Dockerfile Overview

This Dockerfile :
- uses NGINX as the base image
- copies the files from local to the container and host them on port 8080.

```docker
#pulls nginx base image
FROM nginx:alpine

#Copy frontend files from host
COPY ./index.html /usr/share/nginx/html

#using port 80
EXPOSE 80
```

## Usage

1. Clone the Repository
```docker
git clone https://github.com/avinash-gl/docker-projects.git
cd docker-projects/nginx-docker
``` 

2. 🔧 Build the Docker Image
```docker
docker build -t my-nginx-app .
```

3. Run the Container
```docker
docker run -d -p 8080:80 my-nginx-app
```

4. Visit the site in your browser:
```docker
http://localhost:8080
```

## Cleanup

Stop and remove the container:
```docker
docker ps       # Get container ID
docker stop <container_id>
docker rm <container_id>
```

Delete the image:
```docker
docker rmi my-nginx-app
```
