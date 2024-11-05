# Docker

Create the image :
```sh
docker compose build
```
Run the project :
```sh
docker compose up
```
Or in daemon (as a background process) :
```sh
docker compose up -d
```

Show logs (console content) in real time but read-only
```sh
docker logs -f <container_name>
```
Show the running containers list :
```sh
docker ps
```

Show all containers (default shows just running) :
```sh
docker ps --all
```

Other lists :
```sh
docker volume ls
docker network ls
docker image ls
```

> **Docker Compose** is a tool for defining and running multi-container applications. It is the key to unlocking a streamlined and efficient development and deployment experience.

In a ```docker-compose.yaml``` with the following configuration, ```88``` is the external port (exposed) and ```80``` the internal port :
```yaml
ports:
        - '88:80'
```

Execute commands in a daemon container (for exemple, to install npm packages) :
```sh
docker exec -it <container-name-or-id> sh
```

Run the project with the 'npm install' after boot :
```sh
docker run --rm -v "$(pwd)"/app:/data -u 2000:2000 --name node-setup --workdir /data -e npm_config_cache=/data/.npm --env HOME=/data -it node:22-alpine3.20 npm install
```