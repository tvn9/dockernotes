# DOCKER CONTAINER

## Container Commands

Start a web server (nginx)  
```docker
$ docker container run --publish 80:80 nginx                // start a new container from an image 
``` 

Start a web server with --detach option 
```docker
$ docker container run --publish 80:80 --detach nginx       // start a new container in the background
```

Show a list of containers
```docker
$ docker container ls               // show a list of containers
$ docker ps                         // old way
$ docker container ls -a            // show list of running and previously created containers 
```

Stop a running container  
```docker
$ docker container stop 7b19        // stop container with first 4 letter of container ID
```  

Start new container with --name option  
```docker
$ docker container run --publish 80:80 --detach --name webhost nginx       // --name webhost is the name of newly starting container  
```

Show container logs for a specific container  
```docker
$ docker container logs webhost        // show logs from webhost container 
```

