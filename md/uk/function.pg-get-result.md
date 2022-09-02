---
navigation:
  - function.pg-get-pid.md: « pggetpid
  - function.pg-host.md: пгhost »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгgetresult
---
# пгgetresult

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгgetresult — Отримання результату асинхронного запиту

### Опис

```methodsynopsis
pg_get_result(PgSql\Connection $connection): PgSql\Result|false
```

**пгgetresult()** отримує екземпляр [PgSqlResult](class.pgsql-result.md) з асинхронного запиту, запущеного функціями [пгsendquery()](function.pg-send-query.md) [пгsendqueryparams()](function.pg-send-query-params.md) або [пгsendexecute()](function.pg-send-execute.md)

[пгsendquery()](function.pg-send-query.md) та інші функції, що посилають асинхронні запити, може надсилати відразу кілька запитів на сервер. Функція **пгgetresult()** отримає результати всіх запитів по черзі.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

Екземпляр [PgSqlResult](class.pgsql-result.md), або \*\*`false`\*\*коли доступних результатів більше немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSqlResult](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгgetresult()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с сервером");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from authors; select count(*) from authors;");
  }

  $res1 = pg_get_result($dbconn);
  echo "Первый вызов pg_get_result(): $res1\n";
  $rows1 = pg_num_rows($res1);
  echo "$res1 имеет $rows1 записей\n\n";

  $res2 = pg_get_result($dbconn);
  echo "Второй вызов pg_get_result(): $res2\n";
  $rows2 = pg_num_rows($res2);
  echo "$res2 имеет $rows2 записей\n";
?>
```

Результат виконання цього прикладу:

```
Первый вызов pg_get_result(): Resource id #3
Resource id #3 имеет 3 записей

Второй вызов pg_get_result(): Resource id #4
Resource id #4 имеет 1 записей
```

### Дивіться також

-   [пгsendquery()](function.pg-send-query.md) - Надсилає асинхронний запит
