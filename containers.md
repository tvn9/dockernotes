## Container Commands

Start a web server (nginx)  
```docker
% docker container run --publish 80:80 nginx                // start a new container from an image 
``` 

Start a web server with --detach option 
```docker
% docker container run --publish 80:80 --detach nginx       // start a new container in the background
```

Show a list of containers
```docker
% docker container ls               // show a list of containers
% docker ps                         // old way
% docker container ls -a            // show list of running and previously created containers 
```  

Stop a running container  
```docker
% docker container stop 7b19        // stop container with first 4 letters of container ID
```  

Start new container with --name option  
```docker
% docker container run --publish 80:80 --detach --name webhost nginx       // --name webhost is the name of newly starting container  
```

Show container logs for a specific container  
```docker
% docker container logs webhost        // show logs from webhost container 
% docker container logs --help         // use --help to see all log options
```

Cleaning up unwanted containers with 'rm' command, 'rm' will only remove the stop container, running container will stay on the system.  
```docker
% docker container rm a05a 9d7d 7b19 3b62       // remove not-running container by IDs 
```

Remove running containers with 'rm -f' command, this will force the system to remove the specified containers  
```docker
% docker container rm -f 3b62          // remove a running docker container
``` 

Start and stop an existing container  
```docker
% docker start nginx       // start the nginx webserver
% docker stop nginx        // stop the running nginx webserver
```  

Start apache httpd server  
```docker
% docker container run --publish 8080:80 -d --name httpd-apache httpd      // start apache web server on port 8080
```  

Start mysql server  
```docker
% docker container run 3306:3306 -d -p --name db -e MYSQL_RANDOM_ROOT_PASSWORD=yes mysql       // start mysql
```  

### Container CLI Processes Monitoring  

Show running containers processes  
```docker
% docker container ls            // show all running containers
```  

Show container processes 
```docker 
% docker container top mysql     // show processes from mysql container
% docker container top nginx     // show processes from nginx container
% docker container stats nginx   // show configuration status from a container
```   

Show the live container process status such ass CPU, MEM, and NET I/O usage  
```docker
% docker container stats      // show running processes status
```  

### Looking at container from the inside  

```docker 
% docker container run -it       // start new container interactively 
% docker container exec -it      // run additional command in existing container
```  

### Looking at different Linux distros in containers











