---
navigation:
  - ref.pdo-pgsql.md: « PostgreSQL (PDO)
  - pdo.pgsqlcopyfromarray.md: 'PDO::pgsqlCopyFromArray »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: PDO\_PGSQL DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_PGSQL DSN

(PHP 5 >= 5.1.0, PHP 7, PECL PDO\_PGSQL >= 0.1.0)

PDO\_PGSQL DSN — З'єднання з базою даних PostgreSQL

### Опис

Рядок підключення (Data Source Name або DSN) PDO\_PGSQL складається з наступних елементів, розділених пробілом або крапкою з комою:

Префікс DSN

**`pgsql:`**

`host`

Ім'я хоста, на якому розташована база даних.

`port`

Порт, на якому ця база даних чекає на підключення.

`dbname`

Назва бази даних.

`user`

Ім'я користувача для з'єднання. Якщо ви задасте ім'я користувача в DSN, PDO проігнорує значення, передане як параметр конструктору.

`password`

Пароль користувача для з'єднання. Якщо ви задасте пароль у DSN, PDO проігнорує значення, передане як параметр конструктору.

`sslmode`

Режим SSL. Підтримувані значення та їх опис перераховані в [» документації PostgreSQL](http://www.postgresql.org/docs/current/interactive/)

> **Зауваження**: Усі точки з комою в рядку DSN замінюються пробілами, тому що PostgreSQL очікує такий формат. Це означає, що точки з комою в будь-якому з компонентів (наприклад, `password`or`dbname`) не підтримуються.

### Приклади

**Приклад #1 Приклади PDO\_PGSQL DSN**

Наступний приклад демонструє рядок підключення до бази PostgreSQL:

```
pgsql:host=localhost;port=5432;dbname=testdb;user=bruce;password=mypass
```

Наступний приклад демонструє PDO\_PGSQL DSN для підключення до бази даних PostgreSQL за допомогою unix сокету /tmp/.s.PGSQL.5432:

```
pgsql:host=/tmp;port=5432;dbname=testdb;user=bruce;password=mypass
```
