# Yatube API

REST API для социальной сети Yatube.

## Описание

API предоставляет возможности для работы с постами, комментариями, группами и подписками.

## Технологии

- Python 3.11
- Django 3.2.16
- Django REST Framework 3.12.4
- JWT аутентификация

## Установка

1. Клонируйте репозиторий:
```bash
git clone <url-репозитория>
cd api-final-yatube-ad
```

2. Создайте виртуальное окружение и установите зависимости:
```bash
python -m venv venv
source venv/Scripts/activate  # для Windows
pip install -r requirements.txt
```

3. Выполните миграции и запустите сервер:
```bash
cd yatube_api
python manage.py migrate
python manage.py runserver
```

## Примеры запросов

### Получение токена
```
POST /api/v1/jwt/create/
{"username": "user", "password": "pass"}
```

### Работа с постами
```
GET /api/v1/posts/
POST /api/v1/posts/
Authorization: Bearer <token>
{"text": "Текст поста"}
```

### Комментарии
```
GET /api/v1/posts/1/comments/
POST /api/v1/posts/1/comments/
Authorization: Bearer <token>
{"text": "Комментарий"}
```

### Подписки
```
GET /api/v1/follow/
POST /api/v1/follow/
Authorization: Bearer <token>
{"following": "username"}
```

## Документация

Полная документация API: `redoc.yaml`
