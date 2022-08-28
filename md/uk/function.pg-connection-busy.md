Перевіряє, чи зайнято з'єднання на даний момент.

-   [« pg\_connect](function.pg-connect.html)
    
-   [pg\_connection\_reset »](function.pg-connection-reset.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Перевіряє, чи зайнято з'єднання на даний момент.
    

# пгconnectionbusy

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгconnectionbusy - Перевіряє, чи зайнято з'єднання в даний момент.

### Опис

```methodsynopsis
pg_connection_busy(PgSql\Connection $connection): bool
```

**пгconnectionbusy()** визначає, чи зайнято з'єднання в даний момент чи ні. З'єднання працює, коли попередній запит ще виконується. Функція [pg\_get\_result()](function.pg-get-result.html) також блокує з'єднання на час виконання.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

Повертає **`true`**, якщо з'єднання зайнято, інакше **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгconnectionbusy()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединится");
  $bs = pg_connection_busy($dbconn);
  if ($bs) {
      echo 'Соединение занято';
  } else {
     echo 'Соединение не занято';
  }
?>
```

### Дивіться також

-   [pg\_connection\_status()](function.pg-connection-status.html) - Визначає стан підключення
-   [pg\_get\_result()](function.pg-get-result.html) - Отримання результату асинхронного запиту