# vladimirk1211_microservices
vladimirk1211 microservices repository

# monitoring-1
- Создал VM в Yandex.Cloud
- Подключился к Docker host'у
- Запустил Prometheus в контейнере
- Ознакомился с веб интерфейсом Prometheus
- Остановил контейнер с Prometheus
- Создал директорию docker в корне репозитория и переупорядочил структуру директорий
- Создал директорию monitoring/prometheus и сконфигурировал там Dockerfile
- Сконфигурировал monitoring/prometheus/Prometheus.yml
- Собрал образ prometheus
- Собрал образы микросервисов
- Добавил в docker-compose.yml конфигурацию Prometheus
- Запустил микросервисы
- Поработал в веб интерфейсе Prometheus, посмотрел на график при выключенном сервисе
- Добавил в docker-compose.yml конфигурацию node-exporter
- Добавил job в prometheus.yml
- Пересобрал Prometheus
- Пересоздал микросервисы
- Поработал в веб интерфейсе Prometheus
- Запушил собранные образы на DockerHub (https://hub.docker.com/u/vladimirk1211)

# docker-4
- Подключился к Docker host'у
- Запустил контейнер с использованием none-драйвера
- Запустил контейнер с использованием host-драйвера
- Создал bridge-сеть reddit
- Запустил проект на сети reddit
- Запустил проект с сетевыми алиасами
- Создал сети back_net и front_net
- Запустил проект с созданными сетями
- Установил docker-compose
- Сконфигурировал docker-compose.yml
- Задал переменную через export и выполнил `docker-compose up -d`
- Параметризировал docker-compose.yml, описал переменные в .env и выполнил `docker-compose up -d`
- Добавил .env в .gitignore, скопировал .env в .env.example
- Базовое имя проекта образуется из имени каталога и имени контейнера. Его можно задать используя ключ -p в команде `docker-compose up`

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
