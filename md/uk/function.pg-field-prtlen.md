Повертає кількість друкованих символів

-   [« pg\_field\_num](function.pg-field-num.html)
    
-   [pg\_field\_size »](function.pg-field-size.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає кількість друкованих символів
    

# пгfieldprtlen

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldprtlen — Повертає кількість символів, що друкуються.

### Опис

```methodsynopsis
pg_field_prtlen(PgSql\Result $result, int $row_number, mixed $field_name_or_number): int
```

```methodsynopsis
pg_field_prtlen(PgSql\Result $result, mixed $field_name_or_number): int
```

**пгfieldprtlen()** повертає довжину рядка (кількість символів) значення поля під час виведення результату `result`. Рядки нумеруються з нуля. Функція поверне **`false`** у разі виникнення помилки.

`field_name_or_number` Номер чи ім'я вибраного поля. Може передаватися або як int або як string. Якщо передається значення типу int, PHP розпізнає його як номер, інакше як назву поля.

Ознайомтеся з прикладами на сторінці з описом функції [pg\_field\_name()](function.pg-field-name.html)

> **Зауваження**
> 
> Колишня назва функції: **пгfieldprtlen()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`row`

Номер рядка результату запиту з полем. Нумерація рядків починається із нуля. Якщо аргумент не заданий, буде вибрано поточний рядок.

### Значення, що повертаються

Довжина рядка під час виведення значення поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_field\_size()](function.pg-field-size.html) - Повертає розмір поля