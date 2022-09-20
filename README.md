# docker wordpress

Конструктор сайтов Wordpress упакованный в контейнер Docker

---

Подготавливаем структуру:

В файле .env содержатся данные по БД
- Хост
- Имя пользователя
- Пароль пользователя
- Имя БД

```bash
# Папка в которой будут данные сайта и БД
mkdir -p data

# Папка в которой будут данные сайта
mkdir -p data/html

# Папка в которой будет БД
mkdir -p data/mysql

# Даем права на редактирование и создание папок и фалов для Host системы
chmod 777 -R data
```

Запускаем docker контейнеры:
```bash
docker-compose up -d
```

Убеждаемся что запущены контейнеры:
```bash
docker ps | grep wp_
```

Заходми на страницу с Wordpress:
```text
http://localhost:9000/
```

Удалить контейнер:
```bash
docker-compose down
```