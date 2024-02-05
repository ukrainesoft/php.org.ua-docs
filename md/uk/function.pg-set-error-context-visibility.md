---
navigation:
  - function.pg-set-client-encoding.md: « pg\_set\_client\_encoding
  - function.pg-set-error-verbosity.md: pg\_set\_error\_verbosity »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_set\_error\_context\_visibility
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_set\_error\_context\_visibility

(PHP 8 >= 8.3.0)

pg\_set\_error\_context\_visibility — Визначає видимість повідомлень про помилки контексту, що повертаються функціями [pg\_last\_error()](function.pg-last-error.md) і [pg\_result\_error()](function.pg-result-error.md)

### Опис

```methodsynopsis
pg_set_error_context_visibility(PgSql\Connection $connection, int $visibility): int
```

Визначає видимість повідомлень про помилки контексту, що повертаються функціями [pg\_last\_error()](function.pg-last-error.md) і [pg\_result\_error()](function.pg-result-error.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`visibility`

Необхідна видимість: **`PGSQL_SHOW_CONTEXT_NEVER`** **`PGSQL_SHOW_CONTEXT_ERRORS`** або **`PGSQL_SHOW_CONTEXT_ALWAYS`**

### Значення, що повертаються

Функція повертає попередній рівень видимості: **`PGSQL_SHOW_CONTEXT_NEVER`** **`PGSQL_SHOW_CONTEXT_ERRORS`** або **`PGSQL_SHOW_CONTEXT_ALWAYS`**

### Приклади

**Приклад #1 Приклад використання функції** pg\_set\_error\_context\_visibility()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось установить соединение");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  pg_set_error_context_visibility($dbconn, PGSQL_SHOW_CONTEXT_ALWAYS);
  $res1 = pg_get_result($dbconn);
  echo pg_result_error($res1);
?>
```

### Дивіться також

-   [pg\_last\_error()](function.pg-last-error.md) \- Отримує повідомлення про останню помилку на з'єднанні з базою даних.
-   [pg\_result\_error()](function.pg-result-error.md) \- Повертає повідомлення про помилку, пов'язане із запитом результату
