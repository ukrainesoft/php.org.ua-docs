Повертає кількість порушених запитом записів (кортежів)

-   [« Функции PostgreSQL](ref.pgsql.html)
    
-   [пгcancelquery »](function.pg-cancel-query.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає кількість порушених запитом записів (кортежів)
    

# пгaffectedrows

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгaffectedrows — Повертає кількість порушених запитом записів (кортежів)

### Опис

```methodsynopsis
pg_affected_rows(PgSql\Result $result): int
```

**пгaffectedrows()** повертає кількість кортежів (сутностей/записів/рядів) порушених запитом `INSERT` `UPDATE`, і `DELETE` queries.

З версії PostgreSQL 9.0 і більше, сервер повертає кількість вибраних рядів для запиту SELECT. Старіші версії повертають 0 для SELECT.

> **Зауваження**
> 
> Раніше ця функція називалася **пгcmdtuples()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

### Значення, що повертаються

Кількість записів, порушених запитом. Якщо жоден кортеж не торкнувся, функція поверне `0`

### список змін

| Версия | Описание                                                                                                                                           |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгaffectedrows()****

```php
<?php
$result = pg_query($conn, "INSERT INTO authors VALUES ('Orwell', 2002, 'Animal Farm')");

$cmdtuples = pg_affected_rows($result);

echo $cmdtuples . " кортежей затронуто.\n";
?>
```

Результат виконання цього прикладу:

```
1 кортежей затронуто.
```

### Дивіться також

-   [пгquery()](function.pg-query.html) - Виконує запит
-   [пгqueryparams()](function.pg-query-params.html) - Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
-   [пгexecute()](function.pg-execute.html) - Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
-   [пгnumrows()](function.pg-num-rows.html) - Повертає кількість рядків у вибірці