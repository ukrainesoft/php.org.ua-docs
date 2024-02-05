---
navigation:
  - function.pg-connect.md: « pg\_connect
  - function.pg-connection-reset.md: pg\_connection\_reset »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_connection\_busy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_connection\_busy

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_connection\_busy - Перевіряє, чи зайнято з'єднання в даний момент.

### Опис

```methodsynopsis
pg_connection_busy(PgSql\Connection $connection): bool
```

**pg\_connection\_busy()** визначає, чи зайнято з'єднання в даний момент чи ні. З'єднання працює, коли попередній запит ще виконується. Функція [pg\_get\_result()](function.pg-get-result.md) також блокує з'єднання на час виконання.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Повертає **`true`**, якщо з'єднання зайнято, інакше **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_connection\_busy()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединится");
  $bs = pg_connection_busy($dbconn);
  if ($bs) {
      echo 'Соединение занято';
  } else {
     echo 'Соединение не занято';
  }
?>
```

### Дивіться також

-   [pg\_connection\_status()](function.pg-connection-status.md) \- Визначає стан підключення
-   [pg\_get\_result()](function.pg-get-result.md) \- Отримання результату асинхронного запиту
