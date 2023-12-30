# vladimirk1211_microservices
vladimirk1211 microservices repository

# docker-3
- Подключился к Docker host'у
- Скачал архив и подготовил каталог src
- Создал Dockerfile для подкаталогов post-py, comment, ui
- Скачал последний образ MongoDB
- Собрал образы сервисов (при сборке ui использовался кэш)
- Создал сеть для приложения
- Запустил контейнеры
- Проверил, приложение работает
- Поменял содержимое ./ui/Dockerfile
- Пересобрал ui
- Перезапустил контейнеры
- Создал Docker volume reddit_db и подключил его к контейнеру с MongoDB
- Перезапустил приложение с volume

# docker-2
- Создал директорию docker-monolith
- Установил Docker, docker-compose, docker-machine
- Запустил контейнер hello-world
- Попробовал команды docker
- Сохранил результат команды `docker images` в файл `docker-monolith/docker-1.log`
- С помощью Docker machine создал хост в Yandex Cloud
- Создал файлы Dockerfile, mongod.conf, db_config, start.sh и создал образ
- Зарегитрировался в Docker hub и запушил образ
- Выполнил `docker run --name reddit -d -p 9292:9292 <your-login>/otus-reddit:1.0`
- Проверил что в локальный докер скачался загруженный ранее образ и приложение работает.
