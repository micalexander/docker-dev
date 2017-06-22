# docker-dev
A Dev Environment with Alpine, Bash, PHP, Ruby, Node, MariaDB, NGINX, Docker, and Ansible

## Step one

Clone this repo

```
git clone ...
```

## Step two

Enter the repository directory and create a .env file with the follow key/value environment variables. Change "yourusername" to be the username that you want to be created.


```
# The username you want to use
DEV_USER=yourusername
 
# Directory you want to mount and where you can put your bashrc etc...
DEV_DIR=/Users/yourusername/Dropbox/Development
 
# An additional directoy you want to mount (must uncomment this line and the ADDITIONAL_DIR line in the docker-compose.yml
# ADDITIONAL_DIR=/Users/yourusername/
 
# Where you want to put you site for php/nginx
SITES_DIR=/Users/yourusername/Dropbox/Development/www 
 
# Where you want to store your mysql data and mysql env variables
MYSQL_DATA_DIR=/Users/yourusername/Dropbox/Development/mysql/mysql-data 
MYSQL_ROOT_PASSWORD=somerootpassword
MYSQL_USER=yourusername
MYSQL_PASSWORD=someuserpassword

# Points to the docker sock file
DOCKER_SOCK_FILE=/var/run/docker.sock

# Directories that will be mounted making it possible to use ruby, node, and php from inside the bash container
RUBY_LOCAL_DIR=/usr/local/ruby
NODE_LOCAL_DIR=/usr/local/node
PHP_LOCAL_DIR=/usr/local/php
```
 
## Step three
 
From within the directory run
 
```
docker-compose up
```
 
# Usage
 
After following the sets above you can now use the bash container as a dev environment using your username from the steps above like so:

```
docker exec -it -u yourusername bash /bin/bash -l
```
