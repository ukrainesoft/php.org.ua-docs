---
navigation:
  - function.pg-delete.md: « pgdelete
  - function.pg-escape-bytea.md: пгescapebytea »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгendcopy
---
# пгendcopy

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

пгendcopy — Синхронізує з бекендом PostgreSQL

### Опис

```methodsynopsis
pg_end_copy(?PgSql\Connection $connection = null): bool
```

**пгendcopy()** синхронізує дані між фронтендом PostgreSQL (зазвичай процесом веб-сервера) та сервером PostgreSQL після завершення копіювання даних, досконалих за допомогою функції [пгputline()](function.pg-put-line.md). Використання **пгendcopy()** необхідно, щоб уникнути розсинхронізації сервера PostgreSQL з фронтендом та повідомлень про помилки.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгendcopy()****

```php
<?php
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\\.\n");
  pg_end_copy($conn);
?>
```

### Дивіться також

-   [пгputline()](function.pg-put-line.md) - Передає на PostgreSQL сервер рядок із завершальним нулем
