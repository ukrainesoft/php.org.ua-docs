---
navigation:
  - function.pg-delete.md: « pg\_delete
  - function.pg-escape-bytea.md: pg\_escape\_bytea »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_end\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_end\_copy

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

pg\_end\_copy — Синхронізує з бекендом PostgreSQL

### Опис

```methodsynopsis
pg_end_copy(?PgSql\Connection $connection = null): bool
```

**pg\_end\_copy()** синхронізує дані між фронтендом PostgreSQL (зазвичай процесом веб-сервера) та сервером PostgreSQL після завершення копіювання даних, досконалих за допомогою функції [pg\_put\_line()](function.pg-put-line.md)Использование**pg\_end\_copy()** необхідно, щоб уникнути розсинхронізації сервера PostgreSQL з фронтендом та повідомлень про помилки.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_end\_copy()\*\*\*\*

```php
<?php
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\\.\n");
  pg_end_copy($conn);
?>
```

### Дивіться також

-   [pg\_put\_line()](function.pg-put-line.md) \- Передає на PostgreSQL сервер рядок із завершальним нулем
