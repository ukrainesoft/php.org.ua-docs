Зміщує покажчик на рядок вибірки в екземплярі результату запиту

-   [« pg\_result\_error](function.pg-result-error.html)
    
-   [pg\_result\_status »](function.pg-result-status.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Зміщує покажчик на рядок вибірки в екземплярі результату запиту
    

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

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`row`

Кількість рядків, на які потрібно змістити внутрішній покажчик ресурсу [PgSql\\Result](class.pgsql-result.html). Рядки нумеруються з нуля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгresultseek()****

```php
<?php

// Подключение к базе данных
$conn = pg_pconnect("dbname=publisher");

// Выполнение запроса
$result = pg_query($conn, "SELECT author, email FROM authors");

// Перемещаемся сразу на третью строку
// (допускаем, что в результате есть хотя бы три строки)
pg_result_seek($result, 2);

// Выбираем третью строку из результата
$row = pg_fetch_row($result);

?>
```

### Дивіться також

-   [pg\_fetch\_row()](function.pg-fetch-row.html) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_assoc()](function.pg-fetch-assoc.html) - Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [pg\_fetch\_array()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.html) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.html) - Повертає запис із результату запиту