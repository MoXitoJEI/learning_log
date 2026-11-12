# Learning Log

Учебное веб-приложение для ведения журнала изучаемых тем и записей.

## Локальный запуск в Windows (cmd)

1. Откройте cmd и перейдите в папку проекта.
2. Активируйте окружение:

   ll_env\Scripts\activate.bat

3. Установите зависимости:

   python -m pip install -r requirements.txt

4. Примените миграции:

   python manage.py migrate

5. Запустите сервер:

   python manage.py runserver

Откройте http://127.0.0.1:8000/.

## Запуск через Docker Compose

На сервере после настройки файла .env выполните:

    docker compose up -d --build

## Переменные окружения

- DJANGO_SECRET_KEY — секретный ключ Django.
- DJANGO_DEBUG — режим отладки (на сервере False).
- DJANGO_ALLOWED_HOSTS — список разрешённых IP/имён хостов.
- DJANGO_CSRF_TRUSTED_ORIGINS — доверенные источники для CSRF.
- DJANGO_USE_HTTPS — True при работе через HTTPS.
- SQLITE_PATH — путь к файлу SQLite внутри контейнера.
- APP_BIND_IP — адрес привязки внешнего порта.
- APP_PORT — выделенный внешний порт.
