# docker-dev
A Dev Environment with Alpine, Bash, PHP, Ruby, Node, MariaDB, and NGINX

## Step one

Clone this repo

```
git clone ...
```

## Step two

Enter the repository directory and create a .env file with the follow key/value environment variables. Change "yourusername" to be the username that you want to be created.

```
 DEV_USER=yourusername
 DEV_DIR=/Users/yourusername/Dropbox/Development
 ADDITIONAL_DIR=/Users/yourusername/
 SITES_DIR=/Users/yourusername/Dropbox/Development/www
 MYSQL_DATA_DIR=/Users/yourusername/Dropbox/Development/mysql/mysql-data
 MYSQL_ROOT_PASSWORD=somerootpassword
 MYSQL_USER=yourusername
 MYSQL_PASSWORD=someuserpassword
 RUBY_LOCAL_DIR=/usr/local/ruby
 NODE_LOCAL_DIR=/usr/local/node
 PHP_LOCAL_DIR=/usr/local/php
```
 
 ## Step three
 
 From within the directory run
 
 ```
 docker-compose up
 ```
