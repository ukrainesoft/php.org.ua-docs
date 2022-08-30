Повертає всі переходи для часового поясу

-   [« DateTimeZone::getOffset](datetimezone.getoffset.html)
    
-   [DateTimeZone::listAbbreviations »](datetimezone.listabbreviations.html)
    
-   [PHP Manual](index.html)
    
-   [DateTimeZone](class.datetimezone.html)
    
-   Повертає всі переходи для часового поясу
    

# DateTimeZone::getTransitions

# timezonetransitionsget

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DateTimeZone::getTransitions -- timezonetransitionsget — Повертає всі переходи для часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public DateTimeZone::getTransitions(int $timestampBegin = PHP_INT_MIN, int $timestampEnd = PHP_INT_MAX): array|false
```

Процедурний стиль

```methodsynopsis
timezone_transitions_get(DateTimeZone $object, int $timestampBegin = PHP_INT_MIN, int $timestampEnd = PHP_INT_MAX): array|false
```

### Список параметрів

`object`

Тільки для процедурного стилю: об'єкт [DateTimeZone](class.datetimezone.html), що повертається [timezoneopen()](function.timezone-open.html)

`timestampBegin`

Початкова позначка часу.

`timestampEnd`

Кінцева позначка часу.

### Значення, що повертаються

У разі успішного виконання повертає чисельно індексований масив масивів з усіма переходами або **`false`** у разі виникнення помилки. Об'єкти DateTimeZone, що обертають тип 1 (зсув UTC) і тип 2 (скорочення), не містять переходів і виклик цього методу в такому випадку поверне **`false`**

Якщо встановлено параметр `timestampBegin`, то перший запис у повертається масиві буде містити елемент переходу на момент параметра `timestampBegin`

**Структура переходів масиву**

| Ключ | Тип | Описание |
| --- | --- | --- |
| `ts` | int | Мітка часу Unix |
| `time` | string | **`DateTimeInterface::ISO8601_EXPANDED`** (PHP 8.2 і пізніші версії) або **`DateTimeInterface::ISO8601`** (PHP 8.1 і раніше версії) строк часу |
| `offset` | int | Зміщення від UTC за секунди |
| `isdst` | bool | Чи активний літній час |
| `abbr` | string | Абревіатура часового поясу |

### Приклади

**Приклад #1 Приклад використання [timezonetransitionsget()](function.timezone-transitions-get.html)**

```php
<?php
$timezone = new DateTimeZone("Europe/London");
$transitions = $timezone->getTransitions();
print_r(array_slice($transitions, 0, 3));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [ts] => -9223372036854775808
            [time] => -292277022657-01-27T08:29:52+0000
            [offset] => 3600
            [isdst] => 1
            [abbr] => BST
        )

    [1] => Array
        (
            [ts] => -1691964000
            [time] => 1916-05-21T02:00:00+0000
            [offset] => 3600
            [isdst] => 1
            [abbr] => BST
        )

    [2] => Array
        (
            [ts] => -1680472800
            [time] => 1916-10-01T02:00:00+0000
            [offset] => 0
            [isdst] =>
            [abbr] => GMT
        )

)
```

**Приклад #2 Приклад використання [timezonetransitionsget()](function.timezone-transitions-get.html) із заданим параметром `timestampBegin`**

```php
<?php
$timezone = new DateTimeZone("Europe/London");
$transitions = $timezone->getTransitions(time());
print_r(array_slice($transitions, 0, 3));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [ts] => 1654184161
            [time] => 2022-06-02T15:36:01+0000
            [offset] => 3600
            [isdst] => 1
            [abbr] => BST
        )

    [1] => Array
        (
            [ts] => 1667091600
            [time] => 2022-10-30T01:00:00+0000
            [offset] => 0
            [isdst] =>
            [abbr] => GMT
        )

    [2] => Array
        (
            [ts] => 1679792400
            [time] => 2023-03-26T01:00:00+0000
            [offset] => 3600
            [isdst] => 1
            [abbr] => BST
        )

)
```