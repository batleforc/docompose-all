# Docker compose all

Every command need to be run where the docker-comopse file exist.

If your install does not support "docker compose" replace it with "docker-compose" in the following commands.

## run bash

```shell
docker compose run --rm [-v VOLUME...] [-p PORT...] [-e KEY=VAL...] [-l KEY=VALUE...] {service} {command}
docker compose run --rm java8 bash
docker compose run --rm java11scala bash -l
docker compose run --rm -v /mnt/c/Users/s47960/Documents/Git/School/xmldemerde:/app java8 bash
```

## Exec command in a already open service

```shell
docker exec -it {service} {command}
docker exec -it java8 /bin/bash
# Open a bash in java8 previously started
```

## List image (service)

- go
  - go19 = go 1.19
  - go18 = go 1.18
  - go19grpc = go 1.19 with grpc support (protoc, protoc-gen-go)
- java
  - java8 = java 8 with maven 3.8.6
  - java11 = java 11 with maven 3.8.6
  - java14 = java 14 with maven 3.6.3
  - java11scala = based on java11 with scala support (need to be used with "bash -l") (Build directly from the dockerfile)
- node
  - node14 = node 14
  - node16 = node 16
  - node18 = node 18
- python
  - python3 = python 3
  - python2 = python 2
  - python-miniforge = python 3 with miniforge support (Build directly from the dockerfile)
- rust
- tool
  - cassandra and other
  - hadoop and other
  - mariadb
  - minio
  - mongo
  - pgsql
  - pgsqlcli
  - redis
  - rediscli
  - kafka (need zookeeper to be turned on too)
- Helper
  - portainer
  - traefik

## Left to do

- Add latext support
