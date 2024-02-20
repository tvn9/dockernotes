## Basic System Info 

Show docer version and system configuration information  
```docker
% docker version                       // show current running version of the client and the server
% docker info                          // show version and alot more system info
% docker                               // show a list of available management commands and sub commands
% docker ps                            // show all docker running processes
% docker container ls                  // show all docker container processes
% docker container ls -a               // show all docker containers (runing or not runing)
```

## Docker Command Syntax  

Docker commands format: 
```docker
% docker + command + sub-command       // docker + management-command + command
```  

Old and new ways of running docker commands 
```docker
% docker run                           // command syntax from the begining of docker
% docker container run                 // new command syntax 
```

Show the docker pocesses running inside a specific container
```docker
% docker top mongo                      // show all processes in mongo container 
```

Show docker processes from the unix kernel  
```docker
% ps aux                                 // show all system processes
% ps aux | grep mongo                    // find mongo docker processs             
```

