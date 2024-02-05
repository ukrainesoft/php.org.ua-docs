---
navigation:
  - function.pg-num-fields.md: « pg\_num\_fields
  - function.pg-options.md: pg\_options »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_num\_rows

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_num\_rows — Повертає кількість рядків у вибірці

### Опис

```methodsynopsis
pg_num_rows(PgSql\Result $result): int
```

**pg\_num\_rows()** повертає кількість рядків в екземплярі [PgSql\\Result](class.pgsql-result.md)

> **Зауваження** :
> 
> Раніше функція називалася **pg\_numrows()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Кількість рядків у вибірці. У разі виникнення помилки повертає `-1`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_num\_rows()\*\*\*\*

```php
<?php
$result = pg_query($conn, "SELECT 1");

$rows = pg_num_rows($result);

echo "Возвращено строк: " . $rows . ".\n";
?>
```

Результат виконання наведеного прикладу:

```
Возвращено строк: 1.
```

### Дивіться також

-   [pg\_num\_fields()](function.pg-num-fields.md) \- Повертає кількість полів у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.md) \- Повертає кількість порушених запитом записів (кортежів)
