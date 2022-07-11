- [« IntlCalendar::getGreatestMinimum](intlcalendar.getgreatestminimum.md)
- [IntlCalendar::getLeastMaximum »](intlcalendar.getleastmaximum.md)

- [PHP Manual](index.md)
- [IntlCalendar](class.intlcalendar.md)
- отримує набір значень ключових слів мовного стандарту

# IntlCalendar::getKeywordValuesForLocale

(PHP 5 = 5.5.0, PHP 7, PHP 8, PECL = 3.0.0a1)

IntlCalendar::getKeywordValuesForLocale — Отримує набір значень
ключових слів мовного стандарту

### Опис

Об'єктно-орієнтований стиль

public static **IntlCalendar::getKeywordValuesForLocale**(string
`$keyword`, string `$locale`, bool `$onlyCommon`):
[IntlIterator](class.intliterator.md)\|false

Процедурний стиль

**intlcal_get_keyword_values_for_locale**(string `$keyword`, string
`$locale`, bool `$onlyCommon`):
[IntlIterator](class.intliterator.md)\|false

Для заданого ключа мовного стандарту отримує набір значень для
цього ключа, які призведуть до іншої поведінки. На даний момент
підтримується тільки ключове слово calendar.

Для роботи функції потрібен ICU 4.2 або новіший.

### Список параметрів

`keyword`
Ключове слово мовного стандарту, для якого потрібно запросити
релевантні значення. Підтримується тільки calendar.

`locale`
Мовний стандарт, до якого має бути додана пара "ключове
слово/значення".

`onlyCommon`
Визначає, чи відображати лише значення, які зазвичай використовуються для
вказаного мовного стандарту.

### Значення, що повертаються

Ітератор, який видає рядки зі значеннями ключових слів.
стандарту або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання
**IntlCalendar::getKeyworkValuesForLocale()****

` <?phpprint_r(        iterator_to_array(                IntlCalendar::getKeywordValuesForLocale(                        'calendar', 'fa_IR', true)));print_r(        iterator_to_array(                IntlCalendar::getKeywordValuesForLocale(                        'calendar', 'fa_IR', false))); `

Результат виконання цього прикладу:

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
