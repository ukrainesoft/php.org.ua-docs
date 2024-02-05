---
navigation:
  - function.pg-get-pid.md: « pg\_get\_pid
  - function.pg-host.md: pg\_host »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_get\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_get\_result

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_get\_result — Отримання результату асинхронного запиту

### Опис

```methodsynopsis
pg_get_result(PgSql\Connection $connection): PgSql\Result|false
```

**pg\_get\_result()** отримує екземпляр [PgSql\\Result](class.pgsql-result.md)из асинхронного запроса, запущенного функциями[pg\_send\_query()](function.pg-send-query.md) [pg\_send\_query\_params()](function.pg-send-query-params.md) або [pg\_send\_execute()](function.pg-send-execute.md)

[pg\_send\_query()](function.pg-send-query.md) та інші функції, що посилають асинхронні запити, може надсилати відразу кілька запитів на сервер. Функція **pg\_get\_result()** отримає результати всіх запитів по черзі.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.md), либо\*\*`false`\*\*коли доступних результатів більше немає.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_get\_result()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с сервером");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from authors; select count(*) from authors;");
  }

  $res1 = pg_get_result($dbconn);
  echo "Первый вызов pg_get_result(): $res1\n";
  $rows1 = pg_num_rows($res1);
  echo "$res1 имеет $rows1 записей\n\n";

  $res2 = pg_get_result($dbconn);
  echo "Второй вызов pg_get_result(): $res2\n";
  $rows2 = pg_num_rows($res2);
  echo "$res2 имеет $rows2 записей\n";
?>
```

Результат виконання наведеного прикладу:

```
Первый вызов pg_get_result(): Resource id #3
Resource id #3 имеет 3 записей

Второй вызов pg_get_result(): Resource id #4
Resource id #4 имеет 1 записей
```

### Дивіться також

-   [pg\_send\_query()](function.pg-send-query.md) \- Надсилає асинхронний запит
