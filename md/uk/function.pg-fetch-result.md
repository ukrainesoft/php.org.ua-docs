---
navigation:
  - function.pg-fetch-object.md: « pgfetchobject
  - function.pg-fetch-row.md: пгfetchrow »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfetchresult
---
# пгfetchresult

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfetchresult — Повертає запис із результату запиту

### Опис

```methodsynopsis
pg_fetch_result(PgSql\Result $result, int $row, mixed $field): string|false|null
```

```methodsynopsis
pg_fetch_result(PgSql\Result $result, mixed $field): string|false|null
```

**пгfetchresult()** повертає значення комірки таблиці примірника [PgSqlResult](class.pgsql-result.md)

> **Зауваження**
> 
> Колишня назва функції: **пгresult()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено, береться наступний по черзі рядок.

`field`

Ім'я або номер поля значення, що вибирається. Поля нумеруються з нуля.

### Значення, що повертаються

Логічні значення повертаються як "t" чи "f". Інші типи, включаючи масиви, повертаються у вигляді рядків у стандартному форматі PostgreSQL, аналогічно висновку програми **psql**. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків в результаті запиту, та за інших помилок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгfetchresult()****

```php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "Первое поле во второй строчке результата это: ", $val, "\n";
?>
```

Результат виконання цього прикладу:

```
Первое поле во второй строчке результата это: 2
```

### Дивіться також

-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгfetcharray()](function.pg-fetch-array.md) - Повертає рядок результату у вигляді масиву
