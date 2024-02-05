---
navigation:
  - function.date-offset-get.md: « date\_offset\_get
  - function.date-parse.md: date\_parse »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: date\_parse\_from\_format
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# date\_parse\_from\_format

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

date\_parse\_from\_format — Отримання інформації про задану в даному форматі дату

### Опис

```methodsynopsis
date_parse_from_format(string $format, string $datetime): array
```

Повертає асоціативний масив із детальною інформацією про задану дату/час.

### Список параметрів

`format`

Документацию по параметру`format`, смотрите в документации к методу[DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md). Застосовуються самі правила.

`datetime`

Рядок, що становить дату/час.

### Значення, що повертаються

Повертає асоціативний масив із детальною інформацією про задану дату/час.

Масив, що повертається, містить ключі `year` `month` `day` `hour` `minute` `second` `fraction`и`is_localtime`

Якщо присутній `is_localtime`, то`zone_type` вказує тип часового поясу. Для типу (Зміщення UTC) вказується `zone`, добавляется поле`is_dst`; для типа (аббревиатура) добавляются поля`tz_abbr`и`is_dst`; для типа`3`(идентификатор часового пояса) добавляются поля`tz_abbr`и`tz_id`

Якщо у параметрі `datetime` присутні елементи відносного часу, наприклад, `+3 days`, що повертається масив включає вкладений масив з ключем `relative`. Цей масив містить ключі `year` `month` `day` `hour` `minute` `second`, і, якщо необхідно, `weekday`и`weekdays`, Залежно від переданого рядка.

Масив включає поля `warning_count`и`warnings`. Перше вказує, скільки було попереджень. Ключі елементів масиву `warnings` вказують на позицію в цьому параметрі `datetime`, Де відбулося попередження, а рядкове значення описує саме попередження.

Массив также содержит поля`error_count`и`errors`. Перше вказує, скільки помилок було знайдено. Ключі елементів масиву `errors` вказують на позицію в цьому параметрі `datetime`, де сталася помилка, а рядкове значення визначає саму помилку.

**Увага**

Кількість елементів масивів `warnings`и`errors` може бути менше, ніж `warning_count`или`error_count`якщо вони виникли в одній і тій же позиції.

### Помилки

Функція викидає [ValueError](class.valueerror.md), якщо параметр `datetime` містить нульові байти.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.21, 8.1.8, 8.2.0 | Тепер при передачі нульових байтів у параметр `datetime` викидається [ValueError](class.valueerror.md), Який раніше мовчки ігнорувався. |
| 7.2.0 | Елемент `zone` масиву, що повертається, відображає тепер секунди замість хвилин, а його знак інвертується. Наприклад, `-120` тепер буде `7200` |

### Приклади

**Пример #1 Пример использования**date\_parse\_from\_format()\*\*\*\*

```php
<?php
$date = "6.1.2009 13:00+01:00";
print_r(date_parse_from_format("j.n.Y H:iP", $date));
?>
```

Результат виконання наведеного прикладу:

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

**Пример #2 Пример использования**date\_parse\_from\_format()**с предупреждениями**

```php
<?php
$date = "26 August 2022 22:30 pm";
$parsed = date_parse_from_format("j F Y G:i a", $date);

echo "Количество предупреждений: ", $parsed['warning_count'], "\n";
foreach ($parsed['warnings'] as $position => $message) {
    echo "\tПозиция {$position}: {$message}\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Количество предупреждений: 1
    Позиция 23: The parsed time was invalid
```

**Пример #3 Пример использования**date\_parse\_from\_format()\*\* з помилками\*\*

```php
<?php
$date = "26 August 2022 CEST";
$parsed = date_parse_from_format("j F Y H:i", $date);

echo "Количество ошибок: ", $parsed['error_count'], "\n";
foreach ($parsed['errors'] as $position => $message) {
    echo "\tПозиция {$position}: {$message}\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Количество ошибок: 3
    Позиция 15: A two digit hour could not be found
    Позиция 19: Data missing
```

### Дивіться також

-   [DateTimeImmutable::createFromFormat()](datetimeimmutable.createfromformat.md) \- Розбирає рядок з датою згідно з вказаним форматом
-   [checkdate()](function.checkdate.md) \- Перевіряє коректність дати за григоріанським календарем
