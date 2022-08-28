Синхронізує з бекендом PostgreSQL

-   [« pg\_delete](function.pg-delete.html)
    
-   [pg\_escape\_bytea »](function.pg-escape-bytea.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Синхронізує з бекендом PostgreSQL
    

# пгendcopy

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

пгendcopy — Синхронізує з бекендом PostgreSQL

### Опис

```methodsynopsis
pg_end_copy(?PgSql\Connection $connection = null): bool
```

**пгendcopy()** синхронізує дані між фронтендом PostgreSQL (зазвичай процесом веб-сервера) та сервером PostgreSQL після завершення копіювання даних, досконалих за допомогою функції [pg\_put\_line()](function.pg-put-line.html). Використання **пгendcopy()** необхідно, щоб уникнути розсинхронізації сервера PostgreSQL з фронтендом та повідомлень про помилки.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `connection` тепер допускає значення null.                                                                                                                       |

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

-   [pg\_put\_line()](function.pg-put-line.html) - Передає на PostgreSQL сервер рядок із завершальним нулем