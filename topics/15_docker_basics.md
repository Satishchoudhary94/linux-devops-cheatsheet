# 🐳 Docker Basics

- `docker ps` – Show running containers
- `docker ps -a` – Show all containers
- `docker images` – List images
- `docker run -d -p 8080:80 nginx` – Run nginx in detached mode
- `docker stop <container_id>` – Stop a container
- `docker rm <container_id>` – Remove a container
- `docker rmi <image_id>` – Remove image
- `docker exec -it <container_id> bash` – Access container terminal
- `docker build -t myapp .` – Build image from Dockerfile
- `docker-compose up` – Start containers with `docker-compose.yml`
- `docker logs <container_id>` – Show logs
