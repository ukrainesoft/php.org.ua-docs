Повертає стан результату запиту

-   [« pgresultseek](function.pg-result-seek.html)
    
-   [пгselect »](function.pg-select.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Повертає стан результату запиту
    

# пгresultstatus

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгresultstatus — Повернення стану результату запиту

### Опис

```methodsynopsis
pg_result_status(PgSql\Result $result, int $mode = PGSQL_STATUS_LONG): string|int
```

**пгresultstatus()** повертає поточний стан екземпляра [PgSqlResult](class.pgsql-result.html), або тег завершення сервером роботи з цим ресурсом.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`mode`

Приймає одне із двох значень: **`PGSQL_STATUS_LONG`** для отримання числового позначення стану `result`, або **`PGSQL_STATUS_STRING`** для отримання стану теги у вигляді рядка. За замовчуванням використовується **`PGSQL_STATUS_LONG`**

### Значення, що повертаються

Якщо як аргумент передається **`PGSQL_STATUS_LONG`**, то повертається одна з перерахованих констант: **`PGSQL_EMPTY_QUERY`** **`PGSQL_COMMAND_OK`** **`PGSQL_TUPLES_OK`** **`PGSQL_COPY_OUT`** **`PGSQL_COPY_IN`** **`PGSQL_BAD_RESPONSE`** **`PGSQL_NONFATAL_ERROR`** **`PGSQL_FATAL_ERROR`**. В іншому випадку функція поверне рядкове подання стану результату запиту.

### список змін

| Версия | Описание                                                                                                                                         |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгresultstatus()****

```php
<?php

// Подключаемся к базе данных
$conn = pg_pconnect("dbname=publisher");

// Выполняем команду COPY
$result = pg_query($conn, "COPY authors FROM STDIN;");

// Получаем состояние результата запроса
$status = pg_result_status($result);

// Разбираем полученные данные
if ($status == PGSQL_COPY_IN)
   echo "Copy began.";
else
   echo "Copy failed.";

?>
```

Результат виконання цього прикладу:

```
Copy began.
```

### Дивіться також

-   [пгconnectionstatus()](function.pg-connection-status.html) - Визначає стан підключення