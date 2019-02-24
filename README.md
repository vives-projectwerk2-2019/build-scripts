# build-scripts
Docker compose and other build scripts for the entire project.

## Configuration
Update the env files before running.
The ttn listener credentials need to be set before running.

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
docker container exec -it build-scripts_broker_1 bash -l
docker container exec -it build-scripts_listener_1 bash -l
docker container exec -it build-scripts_api_1 bash -l
docker container exec -it build-scripts_db_1 bash -l
docker container exec -it build-scripts_kiosk_1 bash -l
```
Sql shell:
```
docker container exec -it build-scripts_mariadb_1 mysql -u api -p
```
Show ip address:
```
docker container exec -it build-scripts_broker_1 ip a show eth0
docker container exec -it build-scripts_kiosk_1 ip a show eth0
docker container exec -it build-scripts_api_1 ip a show eth0
```
