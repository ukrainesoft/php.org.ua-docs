Повертає кількість полів у вибірці

-   [« pg\_meta\_data](function.pg-meta-data.html)
    
-   [pg\_num\_rows »](function.pg-num-rows.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає кількість полів у вибірці
    

# пгnumfields

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгnumfields — Повертає кількість полів у вибірці

### Опис

```methodsynopsis
pg_num_fields(PgSql\Result $result): int
```

**пгnumfields()** повертає кількість полів (стовпців) в екземплярі [PgSql\\Result](class.pgsql-result.html)

> **Зауваження**
> 
> Раніше функція називалася **пгnumfields()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Кількість полів (стовпців) у вибірці. У разі помилки повертає -1.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_num\_rows()](function.pg-num-rows.html) - Повертає кількість рядків у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.html) - Повертає кількість порушених запитом записів (кортежів)