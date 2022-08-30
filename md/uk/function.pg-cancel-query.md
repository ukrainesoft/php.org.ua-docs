Зупинення асинхронного запиту.

-   [« pgaffectedrows](function.pg-affected-rows.html)
    
-   [пгclientencoding »](function.pg-client-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Зупинення асинхронного запиту.
    

# пгcancelquery

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгcancelquery — Зупинити асинхронний запит.

### Опис

```methodsynopsis
pg_cancel_query(PgSql\Connection $connection): bool
```

**пгcancelquery()** скасовує виконання асинхронного запиту, надісланого функціями [пгsendquery()](function.pg-send-query.html) [пгsendqueryparams()](function.pg-send-query-params.html) або [пгsendexecute()](function.pg-send-execute.html). Неможливо завершити виконання запиту, запущеного функцією [пгquery()](function.pg-query.html)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгcancelquery()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from authors; select count(*) from authors;");
  }

  $res1 = pg_get_result($dbconn);
  echo "Первый запрос к pg_get_result(): $res1\n";
  $rows1 = pg_num_rows($res1);
  echo "$res1 получил $rows1 записей\n\n";

  // Остановка выполняющегося в данный момент запроса.
  // Последует второй запрос, если, конечно, он ещё выполняется.
  pg_cancel_query($dbconn);
?>
```

Результат виконання цього прикладу:

```
Первый запрос к pg_get_result(): Resource id #3
Resource id #3 получил 3 записей
```

### Дивіться також

-   [пгsendquery()](function.pg-send-query.html) - Надсилає асинхронний запит
-   [пгconnectionbusy()](function.pg-connection-busy.html) - Перевіряє, чи зайнято з'єднання на даний момент.