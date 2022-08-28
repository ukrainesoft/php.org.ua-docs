Отримання результату асинхронного запиту

-   [« pg\_get\_pid](function.pg-get-pid.html)
    
-   [pg\_host »](function.pg-host.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Отримання результату асинхронного запиту
    

# пгgetresult

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгgetresult — Отримання результату асинхронного запиту

### Опис

```methodsynopsis
pg_get_result(PgSql\Connection $connection): PgSql\Result|false
```

**пгgetresult()** отримує екземпляр [PgSql\\Result](class.pgsql-result.html) з асинхронного запиту, запущеного функціями [pg\_send\_query()](function.pg-send-query.html) [pg\_send\_query\_params()](function.pg-send-query-params.html) або [pg\_send\_execute()](function.pg-send-execute.html)

[pg\_send\_query()](function.pg-send-query.html) та інші функції, що посилають асинхронні запити, може надсилати відразу кілька запитів на сервер. Функція **пгgetresult()** отримає результати всіх запитів по черзі.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.html), або **`false`**коли доступних результатів більше немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_send\_query()](function.pg-send-query.html) - Надсилає асинхронний запит