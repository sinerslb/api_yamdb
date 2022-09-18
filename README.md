# Проект YaMDb
ТЗ в рамках обучния на курсе Python-разработчик Яндекс.практикума:
написать бэкенд проекта (приложение reviews) и API для него (приложение api) так, чтобы они полностью соответствовали документации.
К проекту по адресу http://127.0.0.1:8000/redoc/ подключена документация API YaMDb. В ней описаны возможные запросы к API и структура ожидаемых ответов. Для каждого запроса указаны уровни прав доступа: пользовательские роли, которым разрешён запрос.
### Как запустить проект:

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate users
```
```
python3 manage.py migrate
```
Запустить проект:

```
python3 manage.py runserver
```
# Примеры запросов

Регистрация нового пользователя:

```
curl -X POST http://127.0.0.1:8000/api/v1/auth/signup/
   -H 'Content-Type: application/json'
   -d '{"email": "string","username": "string"}'
```
Получение JWT-токена

```
curl -X POST http://127.0.0.1:8000/api/v1/auth/token/
   -H 'Content-Type: application/json'
   -d '{"username": "string", "confirmation_code":"string"}'
```

# Авторы
Александр Петров,
Сергей Ларин,
Алексей Андреев.