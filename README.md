# vladimirk1211_microservices
vladimirk1211 microservices repository

# logging-1
- Обновлен код в директории /src
- Выполнена сборка образов при помощи скриптов docker_build.sh
- Подготовлено окружение в Yandex.Cloud
- Сконфигурирован docker/docker-compose-logging.yml
- Сконфигурирован logging/fluentd/Dockerfile
- Сконфигурирован logging/fluentd/fluent.conf
- Собран образ для fluentd
- Настроена сборка с тэгом logging
- Просмотрены логи в терминале
- Сконфигурирован docker/docker-compose.yml
- Поднята инфрастурктура
- Изучен интерфейс Kibana
- Переконфигурирован logging/fluentd/fluent.conf
- Изменен драйвер логирования
- Добавлен фильтр во Fluentd
- Добавлен Grok-шаблон
- Добавлен Zipkin
- Переподнята инфраструктура
- Просмотрены трейсы в Zipkin

# kubernetes-1
- Сконфигурировал файлы deployment.yml
- Подняты две ноды для установки k8s
- Подняты master и worker

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
