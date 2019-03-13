# build-scripts
Docker compose and other build scripts for the entire project.

## Configuration
Update the env files before running.
The ttn listener credentials need to be set before running.

## Building
Build and run:
```
docker-compose -p bug-universal-controller up --build
```
Clean:
```
docker-compose -p bug-universal-controller down
```
## While running:
Bash shell:
```
docker container exec -it bug-universal-controller_broker_1 bash -l
docker container exec -it bug-universal-controller_listener_1 bash -l
docker container exec -it bug-universal-controller_api_1 bash -l
docker container exec -it bug-universal-controller_db_1 bash -l
docker container exec -it bug-universal-controller_kiosk_1 bash -l
```
Sql shell:
```
docker container exec -it bug-universal-controller_db_1 mysql -u api -p
```
Show ip address:
```
docker container exec -it bug-universal-controller_broker_1 ip a
docker container exec -it bug-universal-controller_kiosk_1 ip a
docker container exec -it bug-universal-controller_api_1 ip a
```
Or inspect the networks instead:
```
docker network inspect bug-universal-controller_public
docker network inspect bug-universal-controller_db
docker network inspect bug-universal-controller_api
``
