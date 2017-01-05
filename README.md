# gynsdocker

## Local Data Delete
```sh
rm -rf ./data/
```

## ENV VARIABLE
```sh
export DB_TABLE=project
export DB_USERNAME=gary
export DB_PASS=secret
export MYSQL_CONTAINER_NAME=gynsdocker_mariadb_1
```

## Docker IP
docker inspect --format '{{ .NetworkSettings.Networks.gynsdocker_default.IPAddress }}' gynsdocker_mariadb_1

## up mariadb
docker-compose up -d mariadb
docker-compose --project-name project up -d mariadb

###結果
gynsdocker_mariadb latest    2aa202cb0db4  9 seconds ago       390 MB