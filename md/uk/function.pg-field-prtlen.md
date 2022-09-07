---
navigation:
  - function.pg-field-num.md: « pgfieldnum
  - function.pg-field-size.md: пгfieldsize »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfieldprtlen
---
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

Ознайомтеся з прикладами на сторінці з описом функції [пгfieldname()](function.pg-field-name.md)

> **Зауваження**
> 
> Колишня назва функції: **пгfieldprtlen()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`row`

Номер рядка результату запиту з полем. Нумерація рядків починається із нуля. Якщо аргумент не заданий, буде вибрано поточний рядок.

### Значення, що повертаються

Довжина рядка під час виведення значення поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

  $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
  $i = pg_num_fields($res);
  for ($j = 0; $j < $i; $j++) {
      echo "column $j\n";
      $fieldname = pg_field_name($res, $j);
      echo "fieldname: $fieldname\n";
      echo "printed length: " . pg_field_prtlen($res, $fieldname) . " characters\n";
      echo "storage length: " . pg_field_size($res, $j) . " bytes\n";
      echo "field type: " . pg_field_type($res, $j) . " \n\n";
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

-   [пгfieldsize()](function.pg-field-size.md) - Повертає розмір поля
