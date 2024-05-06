Этот проект представляет собой пример Django-приложения, использующего базу данных PostgreSQL. Ниже приведены инструкции по настройке и запуску проекта.

Шаг 1: Установка зависимостей

pip install django psycopg2


Шаг 2: Настройка базы данных PostgreSQL
Создайте базу данных PostgreSQL для вашего проекта:

createdb home

В файле settings.py вашего Django-проекта укажите параметры подключения к вашей базе данных. Пример:

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'home',
        'USER': 'home',
        'PASSWORD': 'home',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

Шаг 3: Применение миграций
Примените миграции Django для создания необходимых таблиц в базе данных:


python manage.py migrate
python manage.py loaddata fixtures/goods/categories.json
python manage.py loaddata fixtures/goods/products.json


Шаг 4: Запуск сервера разработки

python manage.py runserver

Сервер будет доступен по адресу http://localhost:8000/.
