---
navigation:
  - function.pg-send-query-params.md: « pg\_send\_query\_params
  - function.pg-set-client-encoding.md: pg\_set\_client\_encoding »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_send\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_send\_query

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_send\_query — Надсилає асинхронний запит

### Опис

```methodsynopsis
pg_send_query(PgSql\Connection $connection, string $query): int|bool
```

**pg\_send\_query()** відправляє виконання асинхронний запит. На відміну від [pg\_query()](function.pg-query.md) запит може містити кілька SQL-виражень, розділених крапкою з комою. Для отримання результату запиту скористайтеся функцією [pg\_get\_result()](function.pg-get-result.md)

Виконання запиту не перериває роботу скрипта. Для визначення зайнятості з'єднання (коли запит ще виконується) використовуйте функцію [pg\_connection\_busy()](function.pg-connection-busy.md). Виконання запиту можна перервати функцією [pg\_cancel\_query()](function.pg-cancel-query.md)

Незважаючи на те, що можна надіслати кілька запитів за раз, їх не можна надсилати, поки з'єднання зайняте. В іншому випадку, надісланий запит дочекається завершення попереднього, зітре його результат і запуститься сам. Таким чином, ви втратите дані результату попереднього запиту.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`query`

Один або кілька SQL-виражень, розділених крапкою з комою.

Спецсимволи у рядку запиту мають бути [екрановані](function.pg-escape-string.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, \*\*`false`\*\*или в случае возникновения ошибки. Для получения результата запроса используйте функцию[pg\_get\_result()](function.pg-get-result.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_send\_query()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось подключиться");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from authors; select count(*) from authors;");
  }

  $res1 = pg_get_result($dbconn);
  echo "Первый вызов pg_get_result(): $res1\n";
  $rows1 = pg_num_rows($res1);
  echo "$res1 содержит $rows1 записей\n\n";

  $res2 = pg_get_result($dbconn);
  echo "Второй вызов pg_get_result(): $res2\n";
  $rows2 = pg_num_rows($res2);
  echo "$res2 содержит $rows2 записей\n";
?>
```

Результат виконання наведеного прикладу:

```
Первый вызов pg_get_result(): Resource id #3
Resource id #3 содержит 3 записей

Второй вызов pg_get_result(): Resource id #4
Resource id #4 содержит 1 записей
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_cancel\_query()](function.pg-cancel-query.md) \- Зупинення асинхронного запиту.
-   [pg\_get\_result()](function.pg-get-result.md) \- Отримання результату асинхронного запиту
-   [pg\_connection\_busy()](function.pg-connection-busy.md) \- Перевіряє, чи зайнято з'єднання на даний момент.
