# Общая структура проекта

## Структура файлов

- /back - все сервисы back-end
- /front - все сервисы front-end
- /docker - все файлы для docker compose
- /nginx - все файлы для BFF (пока что nginx)

## Запуск

### Dev

Чтобы запустить с автоматическим билдом

```sh
docker-compose -f ./docker/docker-compose-dev.yaml up --force-recreate --build -d
```

Запуск через обычный билд и ап

```sh
docker-compose -f ./docker/docker-compose-dev.yaml build
docker-compose -f ./docker/docker-compose-dev.yaml up
```

### Prod

```sh
docker-compose -f ./docker/docker-compose.yaml build
docker-compose -f ./docker/docker-compose.yaml up
```
