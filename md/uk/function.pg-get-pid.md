---
navigation:
  - function.pg-get-notify.html: « pggetnotify
  - function.pg-get-result.html: пгgetresult »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгgetpid
---
# пгgetpid

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгgetpid — Отримує ID процесу сервера БД

### Опис

```methodsynopsis
pg_get_pid(PgSql\Connection $connection): int
```

**пгgetpid()** отримує PID сервер бази даних. PID корисний, коли потрібно визначити, який процес надіслав `NOTIFY` повідомлення, прийняте функцією [пгgetnotify()](function.pg-get-notify.md) (точніше дізнатися, сервер його відправив чи якийсь інший процес).

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

ID процесу сервера бази даних.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 PID сервера PostgreSQL**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// PID сервера БД. Сравните его с PID возвращаемым pg_get_notify()
$pid = pg_get_pid($conn);
?>
```

### Дивіться також

-   [пгgetnotify()](function.pg-get-notify.md) - Отримання SQL NOTIFY повідомлення
