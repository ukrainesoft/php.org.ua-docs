---
navigation:
  - ref.pdo-mysql.md: « MySQL (PDO)
  - ref.pdo-sqlsrv.md: MS SQL Server (PDO) »
  - index.md: PHP Manual
  - ref.pdo-mysql.md: MySQL (PDO)
title: PDOMYSQL DSN
---
# PDOMYSQL DSN

(PECL PDOMYSQL >= 0.1.0)

PDOMYSQL DSN — З'єднання з базою даних MySQL

### Опис

Ім'я джерела даних (Data Source Name або DSN) PDOMYSQL складається з наступних елементів:

DSN префікс

DSN-префікс - це **`mysql:`**

`host`

Ім'я хоста, де знаходиться сервер баз даних.

`port`

Номер порту, який слухає сервер бази даних.

`dbname`

Назва бази даних.

`unix_socket`

Сокет MySQL Unix (не повинен використовуватися спільно з `host` або `port`

`charset`

Кодування. Дивіться розділ [Кодування](mysqlinfo.concepts.charset.md) для додаткової інформації.

### Приклади

**Приклад #1 Приклади DNS для PDOMYSQL**

Наступні приклади показують використання PDOMYSQL DSN для з'єднання з базою даних MySQL:

```
mysql:host=localhost;dbname=testdb
```

Більш складний приклад:

```
mysql:host=localhost;port=3307;dbname=testdb
mysql:unix_socket=/tmp/mysql.sock;dbname=testdb
```

### Примітки

> **Зауваження** **Тільки Unix:**
> 
> Якщо ім'я хоста встановлено як `"localhost"`, З'єднання відбувається через сокет домену. Якщо PDOMYSQL скомпільований з використанням libmysqlclient, то шлях до файлу-сокету буде збігатися з шляхом, яким скомпільований libmysqlclient. Якщо PDOMYSQL скомпільований з використанням mysqlnd, значення сокета за умовчанням, може бути виставлено з використанням налаштування [pdomysql.defaultsocket](ref.pdo-mysql.md#ini.pdo-mysql.default-socket)
