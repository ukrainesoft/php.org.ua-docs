Повертає порядковий номер іменованого поля

-   [« pg\_field\_name](function.pg-field-name.html)
    
-   [pg\_field\_prtlen »](function.pg-field-prtlen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає порядковий номер іменованого поля
    

# пгfieldnum

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldnum - Повертає порядковий номер іменованого поля

### Опис

```methodsynopsis
pg_field_num(PgSql\Result $result, string $field): int
```

**пгfieldnum()** поверне порядковий номер поля з ім'ям `field` в результаті запиту `result`

> **Зауваження**
> 
> Колишня назва функції: **пгfieldnum()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Найменування поля. Це ім'я обробляється як ідентифікатор у SQL-команді, тобто воно переводиться в нижній регістр, якщо воно не укладено в подвійні лапки.

### Значення, що повертаються

Номер поля (починаючи з нуля) або -1 у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

  $res = pg_query($dbconn, "select author, year, title from authors where author = 'Orwell'");

  echo "Столбец 'title' - это поле с номером: ", pg_field_num($res, 'title');
?>
```

Результат виконання цього прикладу:

```
Столбец 'title' - это поле с номером: 2
```

### Дивіться також

-   [pg\_field\_name()](function.pg-field-name.html) - Повертає найменування поля