###########
#  BUILD  #
###########
# docker build -t simple-nginx .

###########
#   RUN   #
###########
# docker run --name <container-name> -it --rm -p port:port <loaded-image-name>
#   OR USE DOCKER-COMPOSE

# Base image to loaded
FROM debian

# Maintainer coordinate
MAINTAINER Benjamin BORT

# Always update at first (saving time in case of modification)
RUN apt-get update

RUN apt-get -y install wget
RUN apt-get -y install nginx

# Send script.sh to image
ADD script.sh /usr/bin/script.sh
RUN chmod 755 /usr/bin/script.sh

# Expose a port for our container
EXPOSE 80:80

# Default launched command
# Can be overwritted
CMD ["nginx", "-g", "daemon off;"]

# Default launched command
# Can't be overwritted
#ENTRYPOINT "script.sh"
