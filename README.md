# Проект "API для Yatube"

### Описание

Учебный проект, позволяющий обращаться к API социальной сети "Yatube". Благодаря нему появляется возможность посылать к социальной сети необходимые запросы и быстро получать информацию.

### Установка проекта на локальной машине.

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/TheUncannyMrBean/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```
### Примеры запросов к API
- GET:
```
http://127.0.0.1:8000/api/v1/posts/
```
Получить список всех публикаций. При указании параметров limit и offset выдача должна работать с пагинацией.

- POST:
```
http://127.0.0.1:8000/api/v1/posts/
```
Добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.
```
{
"text": "string",
"image": "string",
"group": 0
}
```
- PUT:
```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.
- PATCH:
```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Частичное обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.
- DELETE:
```
http://127.0.0.1:8000/api/v1/posts/{id}/
```
Удаление публикации по id. Удалить публикацию может только автор публикации. Анонимные запросы запрещены.
### Автор
Александр Голиков

