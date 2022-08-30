Повертає кількість полів у вибірці

-   [« pgmetadata](function.pg-meta-data.html)
    
-   [пгnumrows »](function.pg-num-rows.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Повертає кількість полів у вибірці
    

# пгnumfields

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгnumfields — Повертає кількість полів у вибірці

### Опис

```methodsynopsis
pg_num_fields(PgSql\Result $result): int
```

**пгnumfields()** повертає кількість полів (стовпців) в екземплярі [PgSqlResult](class.pgsql-result.html)

> **Зауваження**
> 
> Раніше функція називалася **пгnumfields()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Кількість полів (стовпців) у вибірці. У разі помилки повертає -1.

### список змін

| Версия | Описание                                                                                                                                         |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пгnumrows()](function.pg-num-rows.html) - Повертає кількість рядків у вибірці
-   [пгaffectedrows()](function.pg-affected-rows.html) - Повертає кількість порушених запитом записів (кортежів)