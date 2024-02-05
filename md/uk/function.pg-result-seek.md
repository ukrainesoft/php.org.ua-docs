---
navigation:
  - function.pg-result-error.md: « pg\_result\_error
  - function.pg-result-status.md: pg\_result\_status »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_result\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_result\_seek

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_result\_seek — Зміщує вказівник на рядок вибірки в екземплярі результату запиту

### Опис

```methodsynopsis
pg_result_seek(PgSql\Result $result, int $row): bool
```

**pg\_result\_seek()** встановлює зміщення внутрішнього покажчика в екземплярі `result`

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Кількість рядків, на які потрібно змістити внутрішній покажчик ресурсу [PgSql\\Result](class.pgsql-result.md). Рядки нумеруються з нуля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_result\_seek()\*\*\*\*

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

-   [pg\_fetch\_row()](function.pg-fetch-row.md) \- Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_assoc()](function.pg-fetch-assoc.md) \- Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
