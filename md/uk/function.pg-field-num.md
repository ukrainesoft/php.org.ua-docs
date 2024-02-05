---
navigation:
  - function.pg-field-name.md: « pg\_field\_name
  - function.pg-field-prtlen.md: pg\_field\_prtlen »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_num
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_num

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_field\_num - Повертає порядковий номер іменованого поля

### Опис

```methodsynopsis
pg_field_num(PgSql\Result $result, string $field): int
```

**pg\_field\_num()** поверне порядковий номер поля з ім'ям `field`в результате запроса`result`

> **Зауваження** :
> 
> Прежнее название функции:**pg\_fieldnum()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Найменування поля. Це ім'я обробляється як ідентифікатор у SQL-команді, тобто воно переводиться в нижній регістр, якщо воно не укладено в подвійні лапки.

### Значення, що повертаються

Номер поля (починаючи з нуля) або -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

  $res = pg_query($dbconn, "select author, year, title from authors where author = 'Orwell'");

  echo "Столбец 'title' - это поле с номером: ", pg_field_num($res, 'title');
?>
```

Результат виконання наведеного прикладу:

```
Столбец 'title' - это поле с номером: 2
```

### Дивіться також

-   [pg\_field\_name()](function.pg-field-name.md) \- Повертає найменування поля
