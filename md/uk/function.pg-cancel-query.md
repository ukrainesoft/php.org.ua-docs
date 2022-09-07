---
navigation:
  - function.pg-affected-rows.md: « pgaffectedrows
  - function.pg-client-encoding.md: пгclientencoding »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгcancelquery
---
# пгcancelquery

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгcancelquery — Зупинити асинхронний запит.

### Опис

```methodsynopsis
pg_cancel_query(PgSql\Connection $connection): bool
```

**пгcancelquery()** скасовує виконання асинхронного запиту, надісланого функціями [пгsendquery()](function.pg-send-query.md) [пгsendqueryparams()](function.pg-send-query-params.md) або [пгsendexecute()](function.pg-send-execute.md). Неможливо завершити виконання запиту, запущеного функцією [пгquery()](function.pg-query.md)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгcancelquery()****

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

Результат виконання цього прикладу:

```
Первый запрос к pg_get_result(): Resource id #3
Resource id #3 получил 3 записей
```

### Дивіться також

-   [пгsendquery()](function.pg-send-query.md) - Надсилає асинхронний запит
-   [пгconnectionbusy()](function.pg-connection-busy.md) - Перевіряє, чи зайнято з'єднання на даний момент.
