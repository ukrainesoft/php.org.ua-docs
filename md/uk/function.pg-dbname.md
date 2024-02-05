---
navigation:
  - function.pg-copy-to.md: « pg\_copy\_to
  - function.pg-delete.md: pg\_delete »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_dbname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_dbname

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_dbname — Визначає ім'я бази даних

### Опис

```methodsynopsis
pg_dbname(?PgSql\Connection $connection = null): string
```

**pg\_dbname()** повертає ім'я бази даних, що відповідає екземпляру PostgreSQL `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Рядок, що містить ім'я бази даних, що відповідає ресурсу `connection`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** pg\_dbname()\*\*\*\*

```php
<?php
  error_reporting(E_ALL);

  pg_connect("host=localhost port=5432 dbname=mary");
  echo pg_dbname(); // mary
?>
```
