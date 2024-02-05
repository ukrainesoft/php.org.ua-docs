---
navigation:
  - intlcalendar.geterrorcode.md: '« IntlCalendar::getErrorCode'
  - intlcalendar.getfirstdayofweek.md: 'IntlCalendar::getFirstDayOfWeek »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getErrorMessage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getErrorMessage

# intlcal\_get\_error\_message

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getErrorMessage -- intlcal\_get\_error\_message — Отримує останнє повідомлення про помилку об'єкта

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public IntlCalendar::getErrorMessage(): string|false
```

Процедурний стиль:

```methodsynopsis
intlcal_get_error_message(IntlCalendar $calendar): string|false
```

Повертає повідомлення про помилку (якщо є), пов'язане з помилкою, про яку повідомляє [IntlCalendar::getErrorCode()](intlcalendar.geterrorcode.md)or[intlcal\_get\_error\_code()](intlcalendar.geterrorcode.md). Якщо пов'язаного повідомлення про помилку немає, буде повернено лише строкове подання імені константи помилки. В іншому випадку, повідомлення про помилку також включає повідомлення, встановлене на стороні прив'язки PHP.

### Список параметрів

`calendar`

Об'єкт календаря в інтерфейс процедурного стилю.

### Значення, що повертаються

Повідомлення про помилку, пов'язане з останньою помилкою, що виникла під час виклику функції цього об'єкта або рядок, що вказує на відсутність помилки. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**IntlCalendar::getErrorMessage()\*\*\*\*

```php
<?php
$cal = IntlCalendar::createInstance('UTC', 'en_US');
var_dump($cal->getErrorMessage());

$cal->getWeekendTransition(IntlCalendar::DOW_WEDNESDAY);
var_dump($cal->getErrorMessage());
```

Результат виконання наведеного прикладу:

```
string(12) "U_ZERO_ERROR"
string(82) "intlcal_get_weekend_transition: Error calling ICU method: U_ILLEGAL_ARGUMENT_ERROR"
```
