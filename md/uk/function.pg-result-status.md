---
navigation:
  - function.pg-result-seek.md: « pg\_result\_seek
  - function.pg-select.md: pg\_select »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_result\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_result\_status

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_result\_status — Повернення стану результату запиту

### Опис

```methodsynopsis
pg_result_status(PgSql\Result $result, int $mode = PGSQL_STATUS_LONG): string|int
```

**pg\_result\_status()** повертає поточний стан екземпляра [PgSql\\Result](class.pgsql-result.md), або тег завершення сервером роботи з цим ресурсом.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`mode`

Приймає одне із двох значень: **`PGSQL_STATUS_LONG`** для отримання числового позначення стану `result`, либо\*\*`PGSQL_STATUS_STRING`\*\* для отримання стану теги у вигляді рядка. За замовчуванням використовується **`PGSQL_STATUS_LONG`**

### Значення, що повертаються

Якщо як аргумент передається **`PGSQL_STATUS_LONG`**, то повертається одна з перерахованих констант: **`PGSQL_EMPTY_QUERY`** **`PGSQL_COMMAND_OK`** **`PGSQL_TUPLES_OK`** **`PGSQL_COPY_OUT`** **`PGSQL_COPY_IN`** **`PGSQL_BAD_RESPONSE`** **`PGSQL_NONFATAL_ERROR`** **`PGSQL_FATAL_ERROR`**. В іншому випадку функція поверне рядкове подання стану результату запиту.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_result\_status()\*\*\*\*

```php
<?php

// Подключаемся к базе данных
$conn = pg_pconnect("dbname=publisher");

// Выполняем команду COPY
$result = pg_query($conn, "COPY authors FROM STDIN;");

// Получаем состояние результата запроса
$status = pg_result_status($result);

// Разбираем полученные данные
if ($status == PGSQL_COPY_IN)
   echo "Copy began.";
else
   echo "Copy failed.";

?>
```

Результат виконання наведеного прикладу:

```
Copy began.
```

### Дивіться також

-   [pg\_connection\_status()](function.pg-connection-status.md) \- Визначає стан підключення
