Повертає конкретне поле зі звіту про помилки

-   [« pg\_query](function.pg-query.html)
    
-   [pg\_result\_error »](function.pg-result-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає конкретне поле зі звіту про помилки
    

# пгresulterrorfield

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгresulterrorfield — Повертає конкретне поле зі звіту про помилки

### Опис

```methodsynopsis
pg_result_error_field(PgSql\Result $result, int $field_code): string|false|null
```

**пгresulterrorfield()** повертає одне з полів звіту про помилки, пов'язаного з екземпляром `result`. Функція підтримується серверами PostgreSQL версій 7.4 та вище. Потрібне поле задається аргументом `field_code`

Функції [pg\_query()](function.pg-query.html) і [pg\_query\_params()](function.pg-query-params.html) у разі помилок повертають **`false`** замість ресурсу. Щоб мати можливість обробляти помилки, користуйтеся функціями [pg\_send\_query()](function.pg-send-query.html) і [pg\_get\_result()](function.pg-get-result.html)

Для отримання додаткової інформації про хід виконання функції, що відмовила [pg\_query()](function.pg-query.html) використовуйте функції [pg\_set\_error\_verbosity()](function.pg-set-error-verbosity.html) і [pg\_last\_error()](function.pg-last-error.html) та обробляйте результат їх виконання.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field_code`

Можливі значення аргументу `field_code` **`PGSQL_DIAG_SEVERITY`** **`PGSQL_DIAG_SQLSTATE`** **`PGSQL_DIAG_MESSAGE_PRIMARY`** **`PGSQL_DIAG_MESSAGE_DETAIL`** **`PGSQL_DIAG_MESSAGE_HINT`** **`PGSQL_DIAG_STATEMENT_POSITION`** **`PGSQL_DIAG_INTERNAL_POSITION`** (для версій PostgreSQL 8.0 та вище), **`PGSQL_DIAG_INTERNAL_QUERY`** (для версій PostgreSQL 8.0 та вище), **`PGSQL_DIAG_CONTEXT`** **`PGSQL_DIAG_SOURCE_FILE`** **`PGSQL_DIAG_SOURCE_LINE`** **`PGSQL_DIAG_SOURCE_FUNCTION`**

### Значення, що повертаються

Повідомлення про помилку із заданого поля у вигляді рядка (string); **`null`**якщо задане поле не існує; **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгresulterrorfield()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  if (!pg_connection_busy($dbconn)) {
      pg_send_query($dbconn, "select * from doesnotexist;");
  }

  $res1 = pg_get_result($dbconn);
  echo pg_result_error_field($res1, PGSQL_DIAG_SQLSTATE);
?>
```

### Дивіться також

-   [pg\_result\_error()](function.pg-result-error.html) - Повертає повідомлення про помилку, пов'язане із запитом результату