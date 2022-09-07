---
navigation:
  - function.pg-copy-to.md: « pgcopyто
  - function.pg-delete.md: пгdelete »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгdbname
---
# пгdbname

(PHP 4, PHP 5, PHP 7, PHP 8)

пгdbname — Визначає ім'я бази даних

### Опис

```methodsynopsis
pg_dbname(?PgSql\Connection $connection = null): string
```

**пгdbname()** повертає ім'я бази даних, що відповідає екземпляру PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я бази даних, що відповідає ресурсу `connection`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгdbname()****

```php
<?php
  error_reporting(E_ALL);

  pg_connect("host=localhost port=5432 dbname=mary");
  echo pg_dbname(); // mary
?>
```
