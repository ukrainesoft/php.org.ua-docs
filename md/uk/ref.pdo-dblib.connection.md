З'єднання з базами даних Microsoft SQL Server та Sybase

-   [« MS SQL Server (PDODBLIB)](ref.pdo-dblib.html)
    
-   [Firebird (PDO) »](ref.pdo-firebird.html)
    
-   [PHP Manual](index.md)
    
-   [MS SQL Server (PDODBLIB)](ref.pdo-dblib.html)
    
-   З'єднання з базами даних Microsoft SQL Server та Sybase
    

# PDODBLIB DSN

(PECL PDODBLIB> = 0.9.0)

PDODBLIB DSN — З'єднання з базами даних Microsoft SQL Server та Sybase

### Опис

Ім'я джерела даних (Data Source Name, DSN) PDODBLIB складається з наступних елементів:

Префікс DSN

Використовуйте префікс DSN **`sybase:`** у випадку, якщо PDODBLIB зібраний із бібліотеками Sybase ct-lib, \*\*`mssql:`\*\*якщо PDODBLIB зібрано з бібліотеками Microsoft SQL Server, або \*\*`dblib:`\*\*якщо PDODBLIB зібраний із бібліотеками FreeTDS.

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

**Приклад #1 Приклади використання PDODBLIB DSN**

Наступні приклади показують PDODBLIB DSN для з'єднання з базами даних Microsoft SQL Server та Sybase:

```
mssql:host=localhost;dbname=testdb
sybase:host=localhost;dbname=testdb
dblib:host=localhost;dbname=testdb
```