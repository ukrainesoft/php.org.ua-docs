---
navigation:
  - function.pg-connection-reset.md: « pg\_connection\_reset
  - function.pg-consume-input.md: pg\_consume\_input »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_connection\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_connection\_status

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_connection\_status — Визначає стан підключення

### Опис

```methodsynopsis
pg_connection_status(PgSql\Connection $connection): int
```

**pg\_connection\_status()** повертає стан переданого як аргумент з'єднання `connection`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

**`PGSQL_CONNECTION_OK`**либо**`PGSQL_CONNECTION_BAD`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_connection\_status()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");
  $stat = pg_connection_status($dbconn);
  if ($stat === PGSQL_CONNECTION_OK) {
      echo 'Статус соединения: доступно';
  } else {
      echo 'Статус соединения: разорвано';
  }
?>
```

### Дивіться також

-   [pg\_connection\_busy()](function.pg-connection-busy.md) \- Перевіряє, чи зайнято з'єднання на даний момент.
