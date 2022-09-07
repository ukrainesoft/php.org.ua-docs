---
navigation:
  - function.pg-send-query-params.md: « pgsendqueryparams
  - function.pg-set-client-encoding.md: пгsetclientencoding »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгsendquery
---
# пгsendquery

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгsendquery — Надсилає асинхронний запит

### Опис

```methodsynopsis
pg_send_query(PgSql\Connection $connection, string $query): int|bool
```

**пгsendquery()** відправляє виконання асинхронний запит. На відміну від [пгquery()](function.pg-query.md) запит може містити кілька SQL-виражень, розділених крапкою з комою. Для отримання результату запиту скористайтеся функцією [пгgetresult()](function.pg-get-result.md)

Виконання запиту не перериває роботу скрипта. Для визначення зайнятості з'єднання (коли запит ще виконується) використовуйте функцію [пгconnectionbusy()](function.pg-connection-busy.md). Виконання запиту можна перервати функцією [пгcancelquery()](function.pg-cancel-query.md)

Незважаючи на те, що можна надіслати кілька запитів за раз, їх не можна надсилати, поки з'єднання зайняте. В іншому випадку, надісланий запит дочекається завершення попереднього, зітре його результат і запуститься сам. Таким чином, ви втратите дані результату попереднього запиту.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

`query`

Один або кілька SQL-виражень, розділених крапкою з комою.

Спецсимволи у рядку запиту мають бути [екрановані](function.pg-escape-string.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, **`false`** або `0` у разі виникнення помилки. Для отримання результату запиту скористайтеся функцією [пгgetresult()](function.pg-get-result.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгsendquery()****

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

Результат виконання цього прикладу:

```
Первый вызов pg_get_result(): Resource id #3
Resource id #3 содержит 3 записей

Второй вызов pg_get_result(): Resource id #4
Resource id #4 содержит 1 записей
```

### Дивіться також

-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгcancelquery()](function.pg-cancel-query.md) - Зупинення асинхронного запиту.
-   [пгgetresult()](function.pg-get-result.md) - Отримання результату асинхронного запиту
-   [пгconnectionbusy()](function.pg-connection-busy.md) - Перевіряє, чи зайнято з'єднання на даний момент.
