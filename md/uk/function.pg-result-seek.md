---
navigation:
  - function.pg-result-error.md: « pgresulterror
  - function.pg-result-status.md: пгresultstatus »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгresultseek
---
# пгresultseek

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгresultseek — Зміщує вказівник на рядок вибірки в екземплярі результату запиту

### Опис

```methodsynopsis
pg_result_seek(PgSql\Result $result, int $row): bool
```

**пгresultseek()** встановлює зміщення внутрішнього покажчика в екземплярі `result`

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`row`

Кількість рядків, на які потрібно змістити внутрішній покажчик ресурсу [PgSqlResult](class.pgsql-result.md). Рядки нумеруються з нуля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгresultseek()****

```php
<?php

// Подключение к базе данных
$conn = pg_pconnect("dbname=publisher");

// Выполнение запроса
$result = pg_query($conn, "SELECT author, email FROM authors");

// Перемещаемся сразу на третью строку
// (допускаем, что в результате есть хотя бы три строки)
pg_result_seek($result, 2);

// Выбираем третью строку из результата
$row = pg_fetch_row($result);

?>
```

### Дивіться також

-   [пгfetchrow()](function.pg-fetch-row.md) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfetchassoc()](function.pg-fetch-assoc.md) - Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [пгfetcharray()](function.pg-fetch-array.md) - Повертає рядок результату у вигляді масиву
-   [пгfetchobject()](function.pg-fetch-object.md) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult()](function.pg-fetch-result.md) - Повертає запис із результату запиту
