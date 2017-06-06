
Docker Tutorial

Documentation  : https://docs.docker.com/
HUB            : https://hub.docker.com/explore/

Useful commands

Docker Basics :
- "ps"                                          : List launched containers
- "ps -a"                                       : List launched and stopped containers
- "stop <container_id> || <container_name>"     : Stop container(s)
- "rm <container_id> || <container_name>"       : Delete container(s)
- "pull <hub_image_name>:tag"                   : Pull image from Docker HUB with 'tag' version (default : latest)
- "images"                                      : List pulled images
- "rmi <image_id> || <image_name>"              : Delete image(s)

Docker :
- "build --help"                                : List all "docker build" options
- "build <Dockerfile_path>"                     : Create image based from the Dockerfile
- "run --help"                                  : List all "docker run" options
- "run <image_id> || <image_name> [command]"    : Start container from designated image and eventually use command
- "run -it"                                     : Interactive mod
- "run --name <container_name>"                 : Will name the created container as designated
- "run -d"                                      : Run image as a daemon
- "run -p port:port"                            : Design ports that are going to be used for the container


Docker-compose :
- "docker-compose"                              : List all docker-compose options
- "docker-compose up"                           : Start docker-compose.yml
- "docker-compose stop"                         : Stop all started container
- "docker-compose up -d"                        : Start docker-compose.yml in daemon mode



TUTO

All those parts only need docker build, docker run or docker-compose commands. No npm install, no apt-get install

PART-1 :
   Simple Dockerfile file used to created and image based on debian running nginx and some simple script
   Simple docker-compose file used to launch the image created by the Dockerfile
   Expose ports : 80

PART-2 :
   No Dockerfile, only docker-compose.yml : we are using default HUB images
   More parameters add to docker-compose.yml, here we create 4 differents containers interacted with each others : mySql, PHP, Nginx, phpMyAdmin
   Containers declaration order matters (php is using mySql, so mySql first...)
   Exposed ports : 80 -> index.php, 8080 -> phpMyAdmin

PART-3 :
   Git clone git@github.com:BenjaminBort/node-test.git
   Basics Dockerfile and docker-compose.yml used in basic nodeJS app
