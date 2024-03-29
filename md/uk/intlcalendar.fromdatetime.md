---
navigation:
  - intlcalendar.fielddifference.md: '« IntlCalendar::fieldDifference'
  - intlcalendar.get.md: 'IntlCalendar::get »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::fromDateTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::fromDateTime

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a2)

IntlCalendar::fromDateTime — Створює IntlCalendar з об'єкта або рядка DateTime

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlCalendar::fromDateTime(DateTime|string $datetime, ?string $locale = null): ?IntlCalendar
```

Процедурний стиль

```methodsynopsis
intlcal_from_date_time(DateTime|string $datetime, ?string $locale = null): ?IntlCalendar
```

Створює об'єкт [IntlCalendar](class.intlcalendar.md) або з об'єкта [DateTime](class.datetime.md), або з рядка, з якого може бути ініціалізований об'єкт [DateTime](class.datetime.md)

Новий календар представлятиме не тільки той самий момент, що й заданий [DateTime](class.datetime.md) (з урахуванням втрати точності для дат у дуже далекому у минулому чи майбутньому), але й той самий часовий пояс (з застереженням, що й використовуватимуться різні бази даних часових поясів, то результати можуть відрізнятися).

### Список параметрів

`datetime`

Об'єкт [DateTime](class.datetime.md) або рядок (string, яка може бути передана в [DateTime::\_\_construct()](datetime.construct.md)

### Значення, що повертаються

Створений об'єкт [IntlCalendar](class.intlcalendar.md)или\*\*`null`\*\* у разі виникнення помилки. Якщо передається рядок (string), викидається будь-який виняток, що виникає всередині конструктора [DateTime](class.datetime.md)

### Приклади

**Приклад #1 Приклад використання** IntlCalendar::fromDateTime()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');

// то же, что и IntlCalendar::fromDateTime(new DateTime(...))
$cal1 = IntlCalendar::fromDateTime('2013-02-28 00:01:02 Europe/Berlin');

// Обратите внимание, что часовой пояс - Europe/Berlin, а не Europe/Lisbon по умолчанию
echo IntlDateFormatter::formatObject($cal1, 'yyyy MMMM d HH:mm:ss VVVV', 'de_DE'), "\n";
```

Результат виконання наведеного прикладу:

```
2013 Februar 28 00:01:02 Deutschland Zeit
```
