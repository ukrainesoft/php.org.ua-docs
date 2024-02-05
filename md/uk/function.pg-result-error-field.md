---
navigation:
  - function.pg-query.md: « pg\_query
  - function.pg-result-error.md: pg\_result\_error »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_result\_error\_field
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_result\_error\_field

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_result\_error\_field — Повертає конкретне поле зі звіту про помилки

### Опис

```methodsynopsis
pg_result_error_field(PgSql\Result $result, int $field_code): string|false|null
```

**pg\_result\_error\_field()** повертає одне з полів звіту про помилки, пов'язаного з екземпляром `result`. Функція підтримується серверами PostgreSQL версій 7.4 та вище. Потрібне поле задається аргументом `field_code`

Функції [pg\_query()](function.pg-query.md) і [pg\_query\_params()](function.pg-query-params.md) у разі помилок повертають **`false`** замість ресурсу. Щоб мати можливість обробляти помилки, користуйтеся функціями [pg\_send\_query()](function.pg-send-query.md) і [pg\_get\_result()](function.pg-get-result.md)

Для отримання додаткової інформації про хід виконання функції, що відмовила [pg\_query()](function.pg-query.md)используйте функции[pg\_set\_error\_verbosity()](function.pg-set-error-verbosity.md) і [pg\_last\_error()](function.pg-last-error.md) та обробляйте результат їх виконання.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field_code`

Можливі значення аргументу `field_code` **`PGSQL_DIAG_SEVERITY`** **`PGSQL_DIAG_SQLSTATE`** **`PGSQL_DIAG_MESSAGE_PRIMARY`** **`PGSQL_DIAG_MESSAGE_DETAIL`** **`PGSQL_DIAG_MESSAGE_HINT`** **`PGSQL_DIAG_STATEMENT_POSITION`** **`PGSQL_DIAG_INTERNAL_POSITION`** (для версій PostgreSQL 8.0 та вище), **`PGSQL_DIAG_INTERNAL_QUERY`** (для версій PostgreSQL 8.0 та вище), **`PGSQL_DIAG_CONTEXT`** **`PGSQL_DIAG_SOURCE_FILE`** **`PGSQL_DIAG_SOURCE_LINE`** **`PGSQL_DIAG_SOURCE_FUNCTION`**

### Значення, що повертаються

Повідомлення про помилку із заданого поля у вигляді рядка (string); \*\*`null`\*\*якщо задане поле не існує; \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_result\_error\_field()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  $res1 = pg_get_result($dbconn);
  echo pg_result_error_field($res1, PGSQL_DIAG_SQLSTATE);
?>
```

### Дивіться також

-   [pg\_result\_error()](function.pg-result-error.md) \- Повертає повідомлення про помилку, пов'язане із запитом результату
