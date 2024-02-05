---
navigation:
  - function.pg-connection-busy.md: « pg\_connection\_busy
  - function.pg-connection-status.md: pg\_connection\_status »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_connection\_reset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_connection\_reset

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_connection\_reset — Скинути з'єднання (перепідключення)

### Опис

```methodsynopsis
pg_connection_reset(PgSql\Connection $connection): bool
```

**pg\_connection\_reset()** скидає підключення. Може бути використана для усунення помилок.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_connection\_reset()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться");
  $dbconn2 = pg_connection_reset($dbconn);
  if ($dbconn2) {
      echo "Успешный сброс\n";
  } else {
      echo "Неудачный сброс\n";
  }
?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.md) \- Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_connection\_status()](function.pg-connection-status.md) \- Визначає стан підключення
