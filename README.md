```
cd api

docker build -t myapp .  // build and image from Dockerfile
docker build -t myapp:v1 .  // build image with a tag
```

```
docker run --name myapp_container myapp_image  // run container
docker run --name container_name image_name:tag_name // run container of a particluar version/tag of image
docker run --name myapp_c2 -p 4050:4000 -d myapp_image  // expose port and detach terminal
docker run --name myapp_c_nodemon -p 4000:4000 --rm myapp:nodemon  // delete container after stopping
docker run --name myapp_c_nodemon -p 4000:4000 --rm -v /Users/baha/code/tutorials/docker-tutorial/api:/app -v /app/node_modules  myapp:nodemon
```

```
docker stop container_name  // stop container
docker start container_name  // start stopped container
docker start -i container_name  // start in interactive mode
```

```
docker images  // list images
docker ps  // list working containers (processes)
docker ps -a // list all containers
docker image rm myapp // if no containers use this image
docker image rm myapp2 -f // force to remove image without deleting containers
docker container rm myapp_c2  // delete container
docker system prune -a  // remove all containers, images and volumes
```