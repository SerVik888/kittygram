# Проект Kittygram

![branch parameter](https://github.com/SerVik888/kittygram_final/actions/workflows/main.yml/badge.svg?branch=main)

![event parameter](https://github.com/SerVik888/kittygram_final/actions/workflows/main.yml/badge.svg?event=push)

### Описание проекта:
Kittygram - Это сеть, где люди могут размещать фотографии и некоторые данные о своих питомцах. Здесь можно добавить, изменить или удалить данные о своих питомцах, но для этого нужно зарегистрироваться иначе данные доступны только для просмотра. Изменять данные чужих питомцев тоже нельзя, они доступны только для просмотра.

### Как запустить проект:
`git clone git@github.com:SerVik888/kittygram_final.git` -> клонировать репозиторий

**При помощи docker**\
    Перед началом нужно установить и запустить Docker.\
    `docker-compose up` -> запустить Docker Compose\
    Открыть новый терминал\
    `docker compose exec backend python manage.py collectstatic` -> cобрать статику Django\
    `docker compose exec backend cp -r /app/collected_static/. /backend_static/static/` -> копируем статику(backend) на volume\
    `docker compose exec backend python manage.py migrate` -> выполнить миграции\
    `docker compose exec backend python manage.py createsuperuser` -> создать суперпользователя

После запуска будут доступны следующие адреса:\
    - регистрация -> http://localhost:9000/ \
    - админка -> http://localhost:9000/admin/

Дополнительные команды для работы:\
    `docker compose up --build` -> пересборка контейнеров\
    `docker-compose stop` -> остановить Docker Compose\
    `docker-compose down` -> остановить Docker Compose и удалить все контейнеры

**Без docker**\
При запуске использовались следующие версии пакетов:
- Nodejs -> v15.9.0
- npm -> 7.5.3
- Python -> 3.9.10
- pip -> 24.0

Запуск **backend**\
Примечание: для того что-бы использовать sqlite3 раскомментируйте этот блок(DATABASE) в файле backend/kittygram_backend/settings и закомментируйте блок с postgresql.

* Если у вас Linux/macOS\
    `python3 -m venv env` -> создать виртуальное окружение\
    `source env/bin/activate` -> активировать виртуальное окружение\
    `python3 -m pip install --upgrade pip` -> обновить установщик\
    `cd backend` -> перейти в папку\
    `pip install -r requirements.txt` -> установить зависимости из файла requirements.txt\
    `python3 manage.py migrate` -> выполнить миграции\
    `python3 manage.py createsuperuser` -> создать суперпользователя\
    `python3 manage.py runserver` -> запустить проект

* Если у вас windows\
    `python -m venv venv` -> создать виртуальное окружение\
    `source venv/Scripts/activate` -> активировать виртуальное окружение\
    `python -m pip install --upgrade pip` -> обновить установщик\
    `pip install -r requirements.txt` -> установить зависимости из файла requirements.txt\
    `cd backend` -> перейти в папку\
    `python manage.py migrate` -> выполнить миграции\
    `python manage.py createsuperuser` -> создать суперпользователя\
    `python manage.py runserver` -> запустить проект

Запуск frontend нужно выполнять в другом терминале

`cd frontend` -> перейти в папку\
`npm i` -> установить зависимости\
`npm run start` -> запуск приложения

После запуска будут доступны следующие адреса:
- регистрация -> http://localhost:3000/
- админка -> http://127.0.0.1:8000/admin/

### Cписок используемых технологий:

- Django
- React
- pytest
- djangorestframework
- Docker

### Как заполнить файл .env:
В проекте есть файлы .env.example и backend/kittygram_backend/.env.example заполните свой по аналогии.

`POSTGRES_DB` - название базы\
`POSTGRES_USER` - пользователь базы\
`POSTGRES_PASSWORD` - пароль к базе\
`DB_NAME` - имя базы\
`DB_HOST` - имя контейнера, где запущен сервер БД\
`DB_PORT` - порт, по которому Django будет обращаться к базе данных
`SECRET_KEY` - Ключ приложения на Django\
`DEBUG` - режит DEBUG\
`ALLOWED_HOSTS` - список разрешённых хостов

Автор: Сафонов Сергей\
Почта: [sergey_safonov86@inbox.ru](mailto:sergey_safonov86@inbox.ru)
