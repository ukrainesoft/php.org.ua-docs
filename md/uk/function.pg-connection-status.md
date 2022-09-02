---
navigation:
  - function.pg-connection-reset.md: « pgconnectionreset
  - function.pg-consume-input.md: пгconsumeinput »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгconnectionstatus
---
# пгconnectionstatus

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгconnectionstatus — Визначає стан підключення

### Опис

```methodsynopsis
pg_connection_status(PgSql\Connection $connection): int
```

**пгconnectionstatus()** повертає стан переданого як аргумент з'єднання `connection`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

**`PGSQL_CONNECTION_OK`** або **`PGSQL_CONNECTION_BAD`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгconnectionstatus()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");
  $stat = pg_connection_status($dbconn);
  if ($stat === PGSQL_CONNECTION_OK) {
      echo 'Статус соединения: доступно';
  } else {
      echo 'Статус соединения: разорвано';
  }
?>
```

### Дивіться також

-   [пгconnectionbusy()](function.pg-connection-busy.md) - Перевіряє, чи зайнято з'єднання на даний момент.
