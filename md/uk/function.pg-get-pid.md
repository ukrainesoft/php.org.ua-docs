Отримує ID процесу сервера БД

-   [« pg\_get\_notify](function.pg-get-notify.html)
    
-   [pg\_get\_result »](function.pg-get-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Отримує ID процесу сервера БД
    

# пгgetpid

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгgetpid — Отримує ID процесу сервера БД

### Опис

```methodsynopsis
pg_get_pid(PgSql\Connection $connection): int
```

**пгgetpid()** отримує PID сервер бази даних. PID корисний, коли потрібно визначити, який процес надіслав `NOTIFY` повідомлення, прийняте функцією [pg\_get\_notify()](function.pg-get-notify.html) (точніше дізнатися, сервер його відправив чи якийсь інший процес).

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

### Значення, що повертаються

ID процесу сервера бази даних.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_get\_notify()](function.pg-get-notify.html) - Отримання SQL NOTIFY повідомлення