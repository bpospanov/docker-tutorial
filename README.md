```
cd api
docker build -t myapp .

docker images
docker run --name myapp_container myapp    # name container
docker ps # processes
docker stop myapp_container
docker run --name myapp_c2 -p 4050:4000 -d myapp    # expose port and detach terminal
docker ps -a  # all containers
docker start myapp_container  # start stopped container
```

