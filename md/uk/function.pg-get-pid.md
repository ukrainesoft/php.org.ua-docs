---
navigation:
  - function.pg-get-notify.md: « pg\_get\_notify
  - function.pg-get-result.md: pg\_get\_result »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_get\_pid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_get\_pid

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_get\_pid — Отримує ID процесу сервера БД

### Опис

```methodsynopsis
pg_get_pid(PgSql\Connection $connection): int
```

**pg\_get\_pid()** отримує PID сервер бази даних. PID корисний, коли потрібно визначити, який процес надіслав `NOTIFY` повідомлення, прийняте функцією [pg\_get\_notify()](function.pg-get-notify.md) (точніше дізнатися, сервер його відправив чи якийсь інший процес).

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

ID процесу сервера бази даних.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 PID сервера PostgreSQL**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// PID сервера БД. Сравните его с PID возвращаемым pg_get_notify()
$pid = pg_get_pid($conn);
?>
```

### Дивіться також

-   [pg\_get\_notify()](function.pg-get-notify.md) \- Отримання SQL NOTIFY повідомлення
