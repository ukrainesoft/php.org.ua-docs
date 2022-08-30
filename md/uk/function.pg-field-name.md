Повертає найменування поля

-   [« pgfieldісnull](function.pg-field-is-null.html)
    
-   [пгfieldnum »](function.pg-field-num.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Повертає найменування поля
    

# пгfieldname

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldname — Повертає назву поля

### Опис

```methodsynopsis
pg_field_name(PgSql\Result $result, int $field): string
```

**пгfieldname()** повертає ім'я поля результату запиту `result` з порядковим номером `field`. Нумерація полів починається із нуля.

> **Зауваження**
> 
> Колишня назва функції: **пгfieldname()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`field`

Номер поля, починаючи з нуля.

### Значення, що повертаються

Найменування поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

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

-   [пгfieldnum()](function.pg-field-num.html) - Повертає порядковий номер іменованого поля