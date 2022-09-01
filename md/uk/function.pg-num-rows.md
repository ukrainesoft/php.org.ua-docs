---
navigation:
  - function.pg-num-fields.html: « pgnumfields
  - function.pg-options.html: пгoptions »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пгnumrows
---
# пгnumrows

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгnumrows — Повертає кількість рядків у вибірці

### Опис

```methodsynopsis
pg_num_rows(PgSql\Result $result): int
```

**пгnumrows()** повертає кількість рядків в екземплярі [PgSqlResult](class.pgsql-result.html)

> **Зауваження**
> 
> Раніше функція називалася **пгnumrows()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Кількість рядків у вибірці. У разі виникнення помилки повертає `-1`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгnumrows()****

```php
<?php
$result = pg_query($conn, "SELECT 1");

$rows = pg_num_rows($result);

echo "Возвращено строк: " . $rows . ".\n";
?>
```

Результат виконання цього прикладу:

```
Возвращено строк: 1.
```

### Дивіться також

-   [пгnumfields()](function.pg-num-fields.html) - Повертає кількість полів у вибірці
-   [пгaffectedrows()](function.pg-affected-rows.html) - Повертає кількість порушених запитом записів (кортежів)
