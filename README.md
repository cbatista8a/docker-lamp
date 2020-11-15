Simple LAMP
==========

Environment variables
----
- MYSQL_ROOT_PASSWORD=root
- MYSQL_DATABASE=prestashop
- MYSQL_USER=admin
- MYSQL_PASSWORD=admin
- MYSQL_ALLOW_EMPTY_PASSWORD=""
- MYSQL_RANDOM_ROOT_PASSWORD=""
- MYSQL_INITDB_SKIP_TZINFO=""


Exposed port and volumes
----

The image exposes ports `80`,`8080`  and `3306`

-Web root [localhost](http://localhost)

-phpMyAdmin [localhost:8080](http://localhost:8080)

The image exports volumes:

* `/var/lib/mysql`, containing MariaDB files and DB.
* `/var/www/html`, used as Apache's [DocumentRoot directory](http://httpd.apache.org/docs/2.4/en/mod/core.html#documentroot).

Please, refer to https://docs.docker.com/storage/volumes for more information on using host volumes.


Use cases
----

#### Create all containers and build images for developing purposes:

```
	docker-compose up -d --build
```
#### Start only apache and php (without Mariadb server) for test purposes:
```
	docker-compose up -d php-apache
```
#### Start All containers:
```
	docker-compose start
```
#### Stop All containers:
```
	docker-compose stop
```
#### Destroy All containers:
```
	docker-compose down
```

Connect to a container terminal
----
#### 
```
docker exec -it container_name bash
```
- See the Doc for more info [Docker exec](https://docs.docker.com/engine/reference/commandline/exec/)

