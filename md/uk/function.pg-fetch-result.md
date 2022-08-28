Повертає запис із результату запиту

-   [« pg\_fetch\_object](function.pg-fetch-object.html)
    
-   [pg\_fetch\_row »](function.pg-fetch-row.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає запис із результату запиту
    

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

**пгfetchresult()** повертає значення комірки таблиці примірника [PgSql\\Result](class.pgsql-result.html)

> **Зауваження**
> 
> Колишня назва функції: **пгresult()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено, береться наступний по черзі рядок.

`field`

Ім'я або номер поля значення, що вибирається. Поля нумеруються з нуля.

### Значення, що повертаються

Логічні значення повертаються як "t" чи "f". Інші типи, включаючи масиви, повертаються у вигляді рядків у стандартному форматі PostgreSQL, аналогічно висновку програми **psql**. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків в результаті запиту, та за інших помилок.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгfetchresult()****

```php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "Первое поле во второй строчке результата это: ", $val, "\n";
?>
```

Результат виконання цього прикладу:

```
Первое поле во второй строчке результата это: 2
```

### Дивіться також

-   [pg\_query()](function.pg-query.html) - Виконує запит
-   [pg\_fetch\_array()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву