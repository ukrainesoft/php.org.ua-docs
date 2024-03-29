---
navigation:
  - datetimezone.gettransitions.md: '« DateTimeZone::getTransitions'
  - datetimezone.listidentifiers.md: 'DateTimeZone::listIdentifiers »'
  - index.md: PHP Manual
  - class.datetimezone.md: DateTimeZone
title: 'DateTimeZone::listAbbreviations'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeZone::listAbbreviations

# timezone\_abbreviations\_list

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

DateTimeZone::listAbbreviations -- timezone\_abbreviations\_list — Повертає асоціативний масив, що містить прапор переходу на літній час, зміщення та ім'я часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static DateTimeZone::listAbbreviations(): array
```

Процедурний стиль

```methodsynopsis
timezone_abbreviations_list(): array
```

Список абревіатур, що повертається, включає всі історичні випадки використання абревіатур, що може призвести до правильних, але заплутаних записів. Існують також протиріччя, оскільки `PST` використовується як у США, так і на Філіппінах.

Тому список, який повертає цю функцію, не підходить для створення масиву з опціями для надання вибору часового поясу користувачам.

> **Зауваження** :
> 
> Дані для функції попередньо компілюються з міркувань продуктивності та не оновлюються при використанні новішої версії [» timezonedb](https://pecl.php.net/package/timezonedb)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив скорочень часових поясів.

### Приклади

**Приклад #1 Приклад использования[timezone\_abbreviations\_list()](function.timezone-abbreviations-list.md)**

```php
<?php
$timezone_abbreviations = DateTimeZone::listAbbreviations();
print_r($timezone_abbreviations["acst"]);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Array
        (
            [dst] => 1
            [offset] => -14400
            [timezone_id] => America/Porto_Acre
        )

    [1] => Array
        (
            [dst] => 1
            [offset] => -14400
            [timezone_id] => America/Eirunepe
        )

    [2] => Array
        (
            [dst] => 1
            [offset] => -14400
            [timezone_id] => America/Rio_Branco
        )

    [3] => Array
        (
            [dst] => 1
            [offset] => -14400
            [timezone_id] => Brazil/Acre
        )

)
```

### Дивіться також

-   [timezone\_identifiers\_list()](function.timezone-identifiers-list.md) \- Псевдонім DateTimeZone::listIdentifiers
