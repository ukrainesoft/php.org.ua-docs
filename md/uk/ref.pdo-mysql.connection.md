---
navigation:
  - ref.pdo-mysql.md: « MySQL (PDO)
  - ref.pdo-sqlsrv.md: MS SQL Server (PDO) »
  - index.md: PHP Manual
  - ref.pdo-mysql.md: MySQL (PDO)
title: PDO\_MYSQL DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_MYSQL DSN

(PECL PDO\_MYSQL >= 0.1.0)

PDO\_MYSQL DSN — З'єднання з базою даних MySQL

### Опис

Ім'я джерела даних (Data Source Name або DSN) PDO\_MYSQL складається з наступних елементів:

DSN префікс

DSN-префікс - це **`mysql:`**

`host`

Ім'я сервера хоста баз даних.

`port`

Номер порту, який слухає сервер бази даних.

`dbname`

Назва бази даних.

`unix_socket`

Сокет MySQL Unix (не можна вказувати спільно з `host`или`port`

`charset`

Кодування. Додаткову інформацію можна знайти в розділі «[Кодування](mysqlinfo.concepts.charset.md)».

### Приклади

**Приклад #1 Приклади DSN для драйвера PDO\_MYSQL**

Наступний приклад показує DSN-ім'я драйвера PDO\_MYSQL для з'єднання з базою даних MySQL:

```
mysql:host=localhost;dbname=testdb
```

Більш повні приклади:

```
mysql:host=localhost;port=3307;dbname=testdb
mysql:unix_socket=/tmp/mysql.sock;dbname=testdb
```

### Примітки

> **Зауваження** **Тільки Unix:**
> 
> Если имя хоста установлено как`«localhost»`, то з'єднання виконується через доменний сокет. Якщо драйвер PDO\_MYSQL скомпілюваний з модулем libmysqlclient, то файл сокету буде знаходитися в папці, скомпільованій libmysqlclient. Якщо PDO\_MYSQL скомпільований з модулем mysqlnd, стандартний сокет можна встановити через директиву [pdo\_mysql.default\_socket](ref.pdo-mysql.md#ini.pdo-mysql.default-socket)
