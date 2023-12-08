### Описание проекта kittygram_final
Kittygram - Это сеть, где люди могут размещать фотографии и некоторые данные о своих питомцах. Здесь можно добавить, изменить или удалить данные о своих питомцах, но для этого нужно зарегистрироваться иначе данные доступны только для просмотра. Изменять данные чужих питомцев тоже нельзя, они доступны только для просмотра.

### Cписок используемых технологий

- Django
- React
- pytest
- djangorestframework
- Docker

### Как запустить проект:

<!-- `git clone git@github.com:SerVik888/kittygram_final.git` -> клонировать репозиторий

`cd api_yamdb` -> перейти в репозиторий

* Если у вас Linux/macOS\
    `python3 -m venv env` -> создать виртуальное окружение\
    `source env/bin/activate` -> активировать виртуальное окружение\
    `python3 -m pip install --upgrade pip` -> обновить установщик\
    `pip install -r requirements.txt` -> установить зависимости из файла requirements.txt\
    `python3 manage.py migrate` -> выполнить миграции\
    `python3 manage.py createsuperuser` -> создать суперпользователя\
    `python3 manage.py runserver` -> запустить проект

* Если у вас windows\
    `python -m venv venv` -> создать виртуальное окружение\
    `source venv/Scripts/activate` -> активировать виртуальное окружение\
    `python -m pip install --upgrade pip` -> обновить установщик\
    `pip install -r requirements.txt` -> установить зависимости из файла requirements.txt\
    `python manage.py migrate` -> выполнить миграции\
    `python manage.py createsuperuser` -> создать суперпользователя\
    `python manage.py runserver` -> запустить проект -->

### Как заполнить файл .env:
В проекте есть файл .env.example заполните свой по аналогии.
"""
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
DB_NAME=kittygram
DB_HOST=db
DB_PORT=5432
"""

Автор:
Сафонов Сергей https://github.com/SerVik888 [sergey_safonov86@inbox.ru](mailto:sergey_safonov86@inbox.ru)