# TaskTracker

Простенький тасктрекер позволяет добавить задачу и описание к ней. 
После выполнения задачи можно сменить её статус на "Выполнено".
Выполненные и невыполненные задачи отображаются в раздельных вкладках.

Проект разворачивается с помощью докера. БД хранится в отельном томе,
поэтому данные после остановки контейнеров не пропадут. 
Контейнер с Nginx распределяет запросы между фронтендом и бекендом. 

## Стек

* Django Rest Framework
* PostgreSQL
* Nginx
* React
* DockerCompose

## Запуск проекта

* Создать `.env` файла на основе `.env.example`

* [Установить докер](https://docs.docker.com/engine/install/)

* Запустить проект
```bash
docker compose -f docker-compose.yml up -d
```

* Выполнить миграции
```bash
docker compose -f docker-compose.yml exec backend python manage.py migrate
```

* Открыть проект
```http request
GET http://127.0.0.1:8000/
```
