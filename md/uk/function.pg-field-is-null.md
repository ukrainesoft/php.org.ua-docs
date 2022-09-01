---
navigation:
  - function.pg-fetch-row.html: « pgfetchrow
  - function.pg-field-name.html: пгfieldname »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пгfieldісnull
---
# пгfieldісnull

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldісnull — Перевірка поля на значення SQL `NULL`

### Опис

```methodsynopsis
pg_field_is_null(PgSql\Result $result, int $row, mixed $field): int
```

```methodsynopsis
pg_field_is_null(PgSql\Result $result, mixed $field): int
```

**пгfieldісnull()** перевіряє, чи містить осередок екземпляра [PgSqlResult](class.pgsql-result.html) значення SQL `NULL`

> **Зауваження**
> 
> Колишня назва функції: **пгfieldisnull()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`row`

Номер рядка результату запиту з полем. Нумерація рядків починається із нуля. Якщо аргумент не заданий, буде вибрано поточний рядок.

`field`

Номер поля (з нуля) як int або ім'я поля як string.

### Значення, що повертаються

Повертає `1`, якщо вибране значення SQL `NULL` `0` для інших значень. Функція поверне **`false`**, якщо номер рядка буде поза допустимим діапазоном та при інших помилках.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгfieldісnull()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die ("Не удалось соединиться с базой");
  $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
  if ($res) {
      if (pg_field_is_null($res, 0, "year") == 1) {
          echo "Значение поля year null.\n";
      }
      if (pg_field_is_null($res, 0, "year") == 0) {
          echo "Значение поля year не null.\n";
    }
 }
?>
```
