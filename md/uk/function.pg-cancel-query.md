---
navigation:
  - function.pg-affected-rows.md: « pg\_affected\_rows
  - function.pg-client-encoding.md: pg\_client\_encoding »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_cancel\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_cancel\_query

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_cancel\_query — Зупинити асинхронний запит.

### Опис

```methodsynopsis
pg_cancel_query(PgSql\Connection $connection): bool
```

**pg\_cancel\_query()** скасовує виконання асинхронного запиту, надісланого функціями [pg\_send\_query()](function.pg-send-query.md) [pg\_send\_query\_params()](function.pg-send-query-params.md) або [pg\_send\_execute()](function.pg-send-execute.md). Неможливо завершити виконання запиту, запущеного функцією [pg\_query()](function.pg-query.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_cancel\_query()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from authors; select count(*) from authors;");
  }

  $res1 = pg_get_result($dbconn);
  echo "Первый запрос к pg_get_result(): $res1\n";
  $rows1 = pg_num_rows($res1);
  echo "$res1 получил $rows1 записей\n\n";

  // Остановка выполняющегося в данный момент запроса.
  // Последует второй запрос, если, конечно, он ещё выполняется.
  pg_cancel_query($dbconn);
?>
```

Результат виконання наведеного прикладу:

```
Первый запрос к pg_get_result(): Resource id #3
Resource id #3 получил 3 записей
```

### Дивіться також

-   [pg\_send\_query()](function.pg-send-query.md) \- Надсилає асинхронний запит
-   [pg\_connection\_busy()](function.pg-connection-busy.md) \- Перевіряє, чи зайнято з'єднання на даний момент.
