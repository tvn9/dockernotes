### Docker Networking  

Showing container tcp port number
```
% docker container port nginx        // nginx-http is the image name
```  

Getting the container IP address  
```
% docker container inspect --format '{{.NetworkSettings.IPAddress}}' nginx        // --format using Go template
```  




