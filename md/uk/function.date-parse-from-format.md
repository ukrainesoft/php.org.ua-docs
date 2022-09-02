---
navigation:
  - function.date-offset-get.md: « dateoffsetget
  - function.date-parse.md: dateparse »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: dateparsefromformat
---
# dateparsefromformat

(PHP 5> = 5.3.0, PHP 7, PHP 8)

dateparsefromformat — Отримання інформації про задану в даному форматі дату

### Опис

```methodsynopsis
date_parse_from_format(string $format, string $datetime): array
```

Повертає асоціативний масив із детальною інформацією про задану дату/час.

### Список параметрів

`format`

Формат, що розпізнається функцією [DateTime::createFromFormat()](datetime.createfromformat.md)

`datetime`

Рядок, що становить дату/час.

### Значення, що повертаються

Повертає асоціативний масив із детальною інформацією про задану дату/час.

### список змін

| Версия | Описание |
| --- | --- |
|  | Елемент `zone` масиву, що повертається, відображає тепер секунди замість хвилин, а його знак інвертується. Наприклад, `-120` тепер буде `7200` |

### Приклади

**Приклад #1 Приклад використання **dateparsefromformat()****

```php
<?php
$date = "6.1.2009 13:00+01:00";
print_r(date_parse_from_format("j.n.Y H:iP", $date));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [year] => 2009
    [month] => 1
    [day] => 6
    [hour] => 13
    [minute] => 0
    [second] => 0
    [fraction] =>
    [warning_count] => 0
    [warnings] => Array
        (
        )

    [error_count] => 0
    [errors] => Array
        (
        )

    [is_localtime] => 1
    [zone_type] => 1
    [zone] => -60
    [is_dst] =>
)
```

### Дивіться також

-   [DateTime::createFromFormat()](datetime.createfromformat.md) - Розбирає рядок з датою згідно з вказаним форматом
-   [checkdate()](function.checkdate.md) - Перевіряє коректність дати за григоріанським календарем
