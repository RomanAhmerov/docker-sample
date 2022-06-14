<h1>Docker</h1>

# Работа с образами
- docker pull node (скачивание образа)
- docker build -t <name> . (сборка катомного образа относитель Dockerfile с кастомным именем)
- docker images (список образов)
- docker rmi <image_id1> <image_id2> (удаление образов)
- docker image prune (удаление всех неиспользованных образов)
- docker tag <old_name> <new_name> (переименование образа)
- docker image inspect <image_name> || <image_id> (информация по образу)

# Работа с контейнерами
- docker ps (список рабочих в данный момент контейнеров)
- docker ps -a (список всех контейнеров)
- docker run -d -p 80:4200 -v logs:/app/data -e PORT1=3000 --env-file ./config/.env --name <custom_name> --rm <image_id> (создание и запуск контейнера по определенному образу, --rm - параметр для удаления контейнера после stop "подробнее смотреть в Makefile")
- docker stop <conteiner_id> (остановка работы контейнера)
- docker start <container_id> (запуск контейнера)
- docker container prune (удаление всех контейнеров)
- docker rm <container_id1> <container_id2> (удаление некоторых контейнеров)

- docker attach <container_id> (подлючиться к процессу "логам" запущенного контейнера)
- docler logs <container_id> (просмотр всех логов определенного контейнера)

# Работа с volumes
- docker volume ls (список volumes)
- docker volume prune (удалить все volumes)
- docker volume rm <volume_name> || <volume_id> (удалить определенный volume)
- docker volume create <volume_name> (создание volume)

# Docker Hub
- docker login (авторизация)
- docker push <username>/<image_name> (отправить образ в Docker репозиторий)
- docker pull <image_name> || <username>/<image_name>
