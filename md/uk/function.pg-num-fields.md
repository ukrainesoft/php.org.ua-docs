---
navigation:
  - function.pg-meta-data.md: « pg\_meta\_data
  - function.pg-num-rows.md: pg\_num\_rows »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_num\_fields

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_num\_fields — Повертає кількість полів у вибірці

### Опис

```methodsynopsis
pg_num_fields(PgSql\Result $result): int
```

**pg\_num\_fields()** повертає кількість полів (стовпців) в екземплярі [PgSql\\Result](class.pgsql-result.md)

> **Зауваження** :
> 
> Раніше функція називалася **pg\_numfields()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Кількість полів (стовпців) у вибірці. У разі помилки повертає -1.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_num\_fields()\*\*\*\*

```php
<?php
$result = pg_query($conn, "SELECT 1, 2");

$num = pg_num_fields($result);

echo "Возвращено полей: " . $num . ".\n";
?>
```

Результат виконання наведеного прикладу:

```
Возвращено полей: 2.
```

### Дивіться також

-   [pg\_num\_rows()](function.pg-num-rows.md) \- Повертає кількість рядків у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.md) \- Повертає кількість порушених запитом записів (кортежів)
