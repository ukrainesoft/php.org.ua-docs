---
navigation:
  - function.pg-field-prtlen.md: « pg\_field\_prtlen
  - function.pg-field-table.md: pg\_field\_table »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_size

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_field\_size — Повертає розмір поля

### Опис

```methodsynopsis
pg_field_size(PgSql\Result $result, int $field): int
```

**pg\_field\_size()** повертає обсяг пам'яті (в байтах), який займає значення поля результату запиту PostgreSQL `result`

> **Зауваження** :
> 
> Прежнее название функции:**pg\_fieldsize()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Порядковий номер поля результату запиту з нуля.

### Значення, що повертаються

Необхідний обсяг пам'яті (байтах) для зберігання значення поля. -1 вказує на змінний розмір поля.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с базой");

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

Результат виконання наведеного прикладу:

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

-   [pg\_field\_prtlen()](function.pg-field-prtlen.md) \- Повертає кількість друкованих символів
-   [pg\_field\_type()](function.pg-field-type.md) \- Повертає ім'я типу заданого поля
