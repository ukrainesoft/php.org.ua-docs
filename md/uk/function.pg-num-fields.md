---
navigation:
  - function.pg-meta-data.md: « pgmetadata
  - function.pg-num-rows.md: пгnumrows »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгnumfields
---
# пгnumfields

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгnumfields — Повертає кількість полів у вибірці

### Опис

```methodsynopsis
pg_num_fields(PgSql\Result $result): int
```

**пгnumfields()** повертає кількість полів (стовпців) в екземплярі [PgSqlResult](class.pgsql-result.md)

> **Зауваження**
> 
> Раніше функція називалася **пгnumfields()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

### Значення, що повертаються

Кількість полів (стовпців) у вибірці. У разі помилки повертає -1.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгnumfields()****

```php
<?php
$result = pg_query($conn, "SELECT 1, 2");

$num = pg_num_fields($result);

echo "Возвращено полей: " . $num . ".\n";
?>
```

Результат виконання цього прикладу:

```
Возвращено полей: 2.
```

### Дивіться також

-   [пгnumrows()](function.pg-num-rows.md) - Повертає кількість рядків у вибірці
-   [пгaffectedrows()](function.pg-affected-rows.md) - Повертає кількість порушених запитом записів (кортежів)
