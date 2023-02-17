# PostgreSQL

## install on docker

```sh
# 생성
docker compose up -d

# 시작
docker compose start

# 종료
docker compose stop

# 삭제(데이터 보존)
docker compose down

# 삭제(데이터 삭제)
docker compose down -v
```

## Postgres cli

```
# shell 접속
docker exec -it postgres bash

# postgres DB 접속
:/# psql -h localhost -U postgres

# 일반 유저 생성
postgres=# CREATE USER kpcuser PASSWORD 'kpcard' SUPERUSER;
postgres=# CREATE DATABASE kpcdb OWNER kpcuser;

# 사용자 조회 쿼리
postgres=# select * from pg_user;
postgres=# select * from pg_database;

# 일반유저 접속
:/# psql -h localhost -U kpcuser -W kpcdb
```

## pgAdmin

```sh
http://localhost:5480/
chris@kpcard.co.kr / password
```

## Monitoring

```sh
# grafana
http://localhost:3000/

postgresql database dashboard template : ID 9628
```