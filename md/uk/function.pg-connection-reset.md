---
navigation:
  - function.pg-connection-busy.html: « pgconnectionbusy
  - function.pg-connection-status.html: пгconnectionstatus »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгconnectionreset
---
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

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пгconnect()](function.pg-connect.md) - Відкриває з'єднання з базою даних PostgreSQL
-   [пгpconnect()](function.pg-pconnect.md) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгconnectionstatus()](function.pg-connection-status.md) - Визначає стан підключення
