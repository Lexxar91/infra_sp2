# API YAMDB
### Описание:
_API для проекта YAMDB - социальной сети, которая собирает отзывы и оценки пользователей на произведения в разных категориях и жанрах._
### Стек технологий:
- Python
- Postgres
- DRF
- Docker
### Документация к API_YAMDB:
Для просмотра документации используйте эндпойнт: *redoc/*
### Установка сервиса: ###
- *Склонируйте репозитрий на свой компьютер* 
- *Создайте .env файл в директории infra/ в котором должны содержаться следующие переменные:*
- ```DB_ENGINE=django.db.backends.postgresql```
- ```DB_NAME= 'название БД'```
- ```POSTGRES_USER= 'ваше имя пользователя'```
- ```POSTGRES_PASSWORD= 'пароль для доступа к БД'```
- ```DB_HOST=db```
- ```DB_PORT=5432```
- Из папки *infra/* соберите образ при помощи docker-compose ```docker-compose up -d --build```
- Примените миграции ```docker-compose exec web python manage.py migrate```
- Соберите статику ```docker-compose exec web python manage.py collectstatic --no-input```
- Для доступа к админке не забудьте создать суперюзера ```docker-compose exec web python manage.py createsuperuser```
