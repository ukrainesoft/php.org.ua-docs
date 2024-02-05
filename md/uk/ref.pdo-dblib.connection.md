---
navigation:
  - ref.pdo-dblib.md: « MS SQL Server (PDO\_DBLIB)
  - ref.pdo-firebird.md: Firebird (PDO) »
  - index.md: PHP Manual
  - ref.pdo-dblib.md: MS SQL Server (PDO\_DBLIB)
title: PDO\_DBLIB DSN
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO\_DBLIB DSN

(PECL PDO\_DBLIB >= 0.9.0)

PDO\_DBLIB DSN — З'єднання з базами даних Microsoft SQL Server та Sybase

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDO\_DBLIB складається з наступних елементів:

Префікс DSN

Используйте префикс DSN\*\*`sybase:`\*\* у випадку, якщо PDO\_DBLIB зібраний із бібліотеками Sybase ct-lib, \*\*`mssql:`\*\*якщо PDO\_DBLIB зібрано з бібліотеками Microsoft SQL Server, або \*\*`dblib:`\*\*якщо PDO\_DBLIB зібраний із бібліотеками FreeTDS.

`host`

Ім'я сервера, на якому знаходиться база даних. Типово 127.0.0.1.

`dbname`

Назва бази даних.

`charset`

Клієнтське кодування.

`appname`

Ім'я програми (використовується в sysprocesses). За промовчанням "PHP Generic DB-lib" або "PHP freetds".

`secure`

На даний момент не використовується.

### Приклади

**Приклад #1 Приклади використання PDO\_DBLIB DSN**

Наступні приклади показують PDO\_DBLIB DSN для з'єднання з базами даних Microsoft SQL Server та Sybase:

```
mssql:host=localhost;dbname=testdb
sybase:host=localhost;dbname=testdb
dblib:host=localhost;dbname=testdb
```
