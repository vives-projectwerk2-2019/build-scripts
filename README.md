# build-scripts
Docker compose and other build scripts for the entire project.

## Building
Build and run:
```
docker-compose up --build
```
Clean:
```
docker-compose down
```
## While running:
Bash shell:
```
docker container exec -it build-scripts_node_1 bash -l
docker container exec -it build-scripts_mariadb_1 bash -l
docker container exec -it build-scripts_kiosk_1 bash -l
```
Sql shell:
```
docker container exec -it build-scripts_mariadb_1 mysql -u api -p
```
