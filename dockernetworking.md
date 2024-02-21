### Docker Networking  

Showing container tcp port number
```
% docker container port nginx        // nginx-http is the image name
```  

Getting the container IP address  
```
% docker container inspect --format '{{.NetworkSettings.IPAddress}}' nginx        // --format using Go template
```  

Using standard network command in container  
```
% ifconfig eth0         // show ip address on ethernet port eth0 
```  

List all network in a container 
``` 
% docker network ls        // list all networks
```  

Inspect a network in the container 
```
% docker network inspect bridge        // inspect bridge network
```

Create a container network 
```
% docker network create myAppNet       // Create myAppNet network
``` 




