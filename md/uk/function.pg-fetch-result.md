---
navigation:
  - function.pg-fetch-object.md: « pg\_fetch\_object
  - function.pg-fetch-row.md: pg\_fetch\_row »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_result

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_fetch\_result — Повертає запис із результату запиту

### Опис

```methodsynopsis
pg_fetch_result(PgSql\Result $result, int $row, mixed $field): string|false|null
```

```methodsynopsis
pg_fetch_result(PgSql\Result $result, mixed $field): string|false|null
```

**pg\_fetch\_result()** повертає значення комірки таблиці примірника [PgSql\\Result](class.pgsql-result.md)

> **Зауваження** :
> 
> Прежнее наименование функции:**pg\_result()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено, береться наступний по черзі рядок.

`field`

Ім'я або номер поля значення, що вибирається. Поля нумеруються з нуля.

### Значення, що повертаються

Логічні значення повертаються як "t" чи "f". Інші типи, включаючи масиви, повертаються у вигляді рядків у стандартному форматі PostgreSQL, аналогічно висновку програми **psql**Значения`NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків в результаті запиту, та за інших помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_fetch\_result()\*\*\*\*

```php
<?php
$db = pg_connect("dbname=users user=me") || die();

$res = pg_query($db, "SELECT 1 UNION ALL SELECT 2");

$val = pg_fetch_result($res, 1, 0);

echo "Первое поле во второй строчке результата это: ", $val, "\n";
?>
```

Результат виконання наведеного прикладу:

```
Первое поле во второй строчке результата это: 2
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
