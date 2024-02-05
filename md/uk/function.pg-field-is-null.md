---
navigation:
  - function.pg-fetch-row.md: « pg\_fetch\_row
  - function.pg-field-name.md: pg\_field\_name »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_is\_null
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_is\_null

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_field\_is\_null — Проверка поля на значение SQL`NULL`

### Опис

```methodsynopsis
pg_field_is_null(PgSql\Result $result, int $row, mixed $field): int
```

```methodsynopsis
pg_field_is_null(PgSql\Result $result, mixed $field): int
```

**pg\_field\_is\_null()** перевіряє, чи містить осередок екземпляра [PgSql\\Result](class.pgsql-result.md)значение SQL`NULL`

> **Зауваження** :
> 
> Прежнее наименование функции:**pg\_fieldisnull()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер рядка результату запиту з полем. Нумерація рядків починається із нуля. Якщо аргумент не заданий, буде вибрано поточний рядок.

`field`

Номер поля (з нуля) як int або ім'я поля як string.

### Значення, що повертаються

Повертає , якщо вибране значення SQL `NULL` для інших значень. Функція поверне **`false`**, якщо номер рядка буде поза допустимим діапазоном та при інших помилках.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_field\_is\_null()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die ("Не удалось соединиться с базой");
  $res = pg_query($dbconn, "select * from authors where author = 'Orwell'");
  if ($res) {
      if (pg_field_is_null($res, 0, "year") == 1) {
          echo "Значение поля year null.\n";
      }
      if (pg_field_is_null($res, 0, "year") == 0) {
          echo "Значение поля year не null.\n";
    }
 }
?>
```
