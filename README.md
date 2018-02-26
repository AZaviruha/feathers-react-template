## Docker management

### Сборка проекта

```sh
docker-compose -f docker-compose.prod.yml up --build --remove-orphans
```

### Удаление всех образов (если вдруг где-то что-то закешировалось намертво)

```sh
docker-compose rm api; docker rmi testapi_api -f
```

### Запуск pgsql для доступа к PostgreSQL-серверну внутри докера

```sh
docker run -it --rm --net=test_backend  postgres:9.6  psql -h test_db_1 -U test
```
