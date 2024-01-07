Домашнее задание к лекции «Docker Compose»
Реализован работа сервера из домашего задания CRUD: Склады и запасы с помощь котейниизации с использованием:

Nginx
PostgreSQL запускается до Django.
Django запускается через Gunicorn
контейниеры Docker

Docerfile для django в директории stocks_products
Docerfile для nginx в директории nginx
Конфигурация для nginx в директории nginx
Настройки для базы данных следует указать в файле переменых окружения .env.db
Права доступа для django следует указать в файле переменных окружения .env.dev
Docer-compose файл в корне проекта
Для проверки работоспособности сревера реализована загрузка вебстраницы с сообщением "Stock logistic!!!"

Для проверки работсопосбности REST API можно использовать команды из requests-examples.http

Развёртывание проекта
Для развёртывания могут потребоваться sudo права. Команды следует выполнять в корневом каталоге проекта.

сборка:
 сборка docker-compose
запук:
 docker-compose up -d
применение миграций
 docker-compose exec web python manage.py migrate --noinput
остановка сервера и удаление контейнеров:
docker-compose down -v