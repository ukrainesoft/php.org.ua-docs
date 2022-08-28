Визначає стан підключення

-   [« pg\_connection\_reset](function.pg-connection-reset.html)
    
-   [pg\_consume\_input »](function.pg-consume-input.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Визначає стан підключення
    

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

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

**`PGSQL_CONNECTION_OK`** або **`PGSQL_CONNECTION_BAD`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_connection\_busy()](function.pg-connection-busy.html) - Перевіряє, чи зайнято з'єднання на даний момент.