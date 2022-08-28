Повертає кількість рядків у вибірці

-   [« pg\_num\_fields](function.pg-num-fields.html)
    
-   [pg\_options »](function.pg-options.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає кількість рядків у вибірці
    

# пгnumrows

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгnumrows — Повертає кількість рядків у вибірці

### Опис

```methodsynopsis
pg_num_rows(PgSql\Result $result): int
```

**пгnumrows()** повертає кількість рядків в екземплярі [PgSql\\Result](class.pgsql-result.html)

> **Зауваження**
> 
> Раніше функція називалася **пгnumrows()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Кількість рядків у вибірці. У разі виникнення помилки повертає `-1`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_num\_fields()](function.pg-num-fields.html) - Повертає кількість полів у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.html) - Повертає кількість порушених запитом записів (кортежів)