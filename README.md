# MySQL-DCA
mysql-dca  MySQL docker container architecture

# Build Docker image
```
docker build -t mysql-dca .
```
# Run MYSQL Docker container as root
```
docker run -d -p 0.0.0.0:3306:3306 -e MYSQL_ROOT_PASSWORD=unixlabs mysql-dca
```
# Run MYSQL Docker container as user
```
docker run -d -p 0.0.0.0:3306:3306 -e MYSQL_ROOT_PASSWORD=unixlabs MYSQL_USER=unixlabs mysql-dca
```
# Run MYSQL Docker container as user and create a new database 
```
docker run -d -p 0.0.0.0:3306:3306 -e MYSQL_ROOT_PASSWORD=unixlabs MYSQL_USER=unixlabs MYSQL_DATABASE=unixlabs mysql-dca
```

# Environment variables

MYSQL_ROOT_PASSWORD: The password for the root user. Defaults to a blank password

MYSQL_DATABASE: A database to automatically create. If not provided, does not create a database.

MYSQL_USER: A user to create that has access to the database specified by MYSQL_DATABASE.

MYSQL_PASSWORD: The password for MYSQL_USER. Defaults to a blank password.
