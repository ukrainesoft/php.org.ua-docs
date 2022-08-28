Повертає розмір поля

-   [« pg\_field\_prtlen](function.pg-field-prtlen.html)
    
-   [pg\_field\_table »](function.pg-field-table.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає розмір поля
    

# пгfieldsize

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldsize — Повертає розмір поля

### Опис

```methodsynopsis
pg_field_size(PgSql\Result $result, int $field): int
```

**пгfieldsize()** повертає обсяг пам'яті (в байтах), який займає значення поля результату запиту PostgreSQL `result`

> **Зауваження**
> 
> Колишня назва функції: **пгfieldsize()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Порядковий номер поля результату запиту з нуля.

### Значення, що повертаються

Необхідний обсяг пам'яті (байтах) для зберігання значення поля. -1 вказує на змінний розмір поля.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с базой");

  $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
  $i = pg_num_fields($res);
  for ($j = 0; $j < $i; $j++) {
      echo "column $j\n";
      $fieldname = pg_field_name($res, $j);
      echo "fieldname: $fieldname\n";
      echo "printed length: " . pg_field_prtlen($res, $fieldname) . " characters\n";
      echo "storage length: " . pg_field_size($res, $j) . " bytes\n";
      echo "field type: " . pg_field_type($res, $j) . " \n\n";
  }
?>
```

Результат виконання цього прикладу:

```
column 0
fieldname: author
printed length: 6 characters
storage length: -1 bytes
field type: varchar

column 1
fieldname: year
printed length: 4 characters
storage length: 2 bytes
field type: int2

column 2
fieldname: title
printed length: 24 characters
storage length: -1 bytes
field type: varchar
```

### Дивіться також

-   [pg\_field\_prtlen()](function.pg-field-prtlen.html) - Повертає кількість друкованих символів
-   [pg\_field\_type()](function.pg-field-type.html) - Повертає ім'я типу заданого поля