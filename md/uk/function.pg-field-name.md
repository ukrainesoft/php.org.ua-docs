---
navigation:
  - function.pg-field-is-null.md: « pg\_field\_is\_null
  - function.pg-field-num.md: pg\_field\_num »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_name

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_field\_name — Повертає назву поля

### Опис

```methodsynopsis
pg_field_name(PgSql\Result $result, int $field): string
```

\*\*pg\_field\_name()\*\*возвращает имя поля результата запроса`result` з порядковим номером `field`. Нумерація полів починається із нуля.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_fieldname()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Номер поля, починаючи з нуля.

### Значення, що повертаються

Найменування поля.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [pg\_field\_num()](function.pg-field-num.md) \- Повертає порядковий номер іменованого поля
