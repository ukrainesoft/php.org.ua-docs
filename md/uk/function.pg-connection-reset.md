Скидання підключення (перепідключення)

-   [« pg\_connection\_busy](function.pg-connection-busy.html)
    
-   [pg\_connection\_status »](function.pg-connection-status.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Скидання підключення (перепідключення)
    

# пгconnectionreset

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгconnectionreset — Скинути з'єднання (перепідключення)

### Опис

```methodsynopsis
pg_connection_reset(PgSql\Connection $connection): bool
```

**пгconnectionreset()** скидає підключення. Може бути використана для усунення помилок.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгconnectionreset()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");
  $dbconn2 = pg_connection_reset($dbconn);
  if ($dbconn2) {
      echo "Успешный сброс\n";
  } else {
      echo "Неудачный сброс\n";
  }
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.html) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_connection\_status()](function.pg-connection-status.html) - Визначає стан підключення