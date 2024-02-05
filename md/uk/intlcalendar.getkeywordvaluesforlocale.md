---
navigation:
  - intlcalendar.getgreatestminimum.md: '« IntlCalendar::getGreatestMinimum'
  - intlcalendar.getleastmaximum.md: 'IntlCalendar::getLeastMaximum »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getKeywordValuesForLocale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getKeywordValuesForLocale

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getKeywordValuesForLocale — Отримує набір значень ключових слів мовного стандарту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlCalendar::getKeywordValuesForLocale(string $keyword, string $locale, bool $onlyCommon): IntlIterator|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_keyword_values_for_locale(string $keyword, string $locale, bool $onlyCommon): IntlIterator|false
```

Для заданого ключа мовного стандарту отримує набір значень цього ключа, які призведуть до іншого поведінки. На даний момент підтримується лише ключове слово `'calendar'`

Для роботи функції потрібен ICU 4.2 або новіший.

### Список параметрів

`keyword`

Ключове слово мовного стандарту, для якого потрібно задати релевантні значення. Підтримується лише `'calendar'`

`locale`

Мовний стандарт, до якого має бути додано пару "ключове слово/значення".

`onlyCommon`

Визначає, чи відображати лише значення, які зазвичай використовуються для зазначеного мовного стандарту.

### Значення, що повертаються

Ітератор, який видає рядки зі значеннями ключових слів мовного стандарту або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**IntlCalendar::getKeyworkValuesForLocale()\*\*\*\*

```php
<?php
print_r(
        iterator_to_array(
                IntlCalendar::getKeywordValuesForLocale(
                        'calendar', 'fa_IR', true)));
print_r(
        iterator_to_array(
                IntlCalendar::getKeywordValuesForLocale(
                        'calendar', 'fa_IR', false)));
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => persian
    [1] => gregorian
    [2] => islamic
    [3] => islamic-civil
)
Array
(
    [0] => persian
    [1] => gregorian
    [2] => islamic
    [3] => islamic-civil
    [4] => japanese
    [5] => buddhist
    [6] => roc
    [7] => hebrew
    [8] => chinese
    [9] => indian
    [10] => coptic
    [11] => ethiopic
    [12] => ethiopic-amete-alem
)
```
