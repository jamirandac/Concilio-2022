# Concilio-2022

## Docker
### Networking

Ejecutar contenedor

`docker run --rm --name nettools -p 127.0.0.1:2222:22 -itd net-tools:1.5.0`

Ingresar al contenedor

`docker exec -it nettools bash`

Más información: [docker-network-tools](https://github.com/Someguy123/docker-networktools)

### Bases de datos

MySQL

Ejecutar contenedor MySQL

`docker run --rm --name some-mysql -e MYSQL_ROOT_PASSWORD=smu_password -d mysql:latest`

Usar contenedor

`docker exec -it some-mysql mysql -u root -p`

Realizar consultas sin entrar al contenedor

`docker exec -it some-mysql mysql -u root -psmu_password -e "show databases"`

Más información: [Docker MySQL](https://hub.docker.com/_/mysql)

### Compartir archivos

`docker run --rm --name nettools -p 127.0.0.1:2222:22 -itd -v $(pwd)/:/home/  net-tools:1.5.0`

