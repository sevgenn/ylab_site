# Сайт кулинарных рецептов

Сайт написан с использованием Django

## Запуск проекта

#### Создать базу данных Postgresql
psql -U postgres

CREATE DATABASE cookbook;

CREATE USER admin with NOSUPERUSER PASSWORD 'admin';

GRANT ALL PRIVILEGES ON DATABASE cookbook TO admin;

\q

-------------------

## Запуск контейнера Docker

В корне проекта site_docker выпонить:

docker-compose up --build

Внутри контейнера выполнить:

docker-compose exec app bash
#### Применение миграций
bash

python manage.py migrate
#### Добавление данных в базу
bash

python manage.py loaddata data_db.json

Проект запускается на http://127.0.0.1:8000


(В базе уже предустановлен администратор:
admin: пароль admin
и пользователь с ограниченными правами:
user1: пароль 4esz5rdx)