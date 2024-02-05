---
navigation:
  - intlcalendar.roll.md: '« IntlCalendar::roll'
  - intlcalendar.setdate.md: 'IntlCalendar::setDate »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::set

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::set — Встановлює поле часу або кілька спільних полів.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::set(int $field, int $value): true
```

```methodsynopsis
public IntlCalendar::set(    int $year,    int $month,    int $dayOfMonth = NULL,    int $hour = NULL,    int $minute = NULL,    int $second = NULL): true
```

Процедурний стиль

```methodsynopsis
intlcal_set(IntlCalendar $cal, int $field, int $value): true
```

```methodsynopsis
intlcal_set(    IntlCalendar $cal,    int $year,    int $month,    int $dayOfMonth = NULL,    int $hour = NULL,    int $minute = NULL,    int $second = NULL): bool
```

Встановлює або конкретне поле задане значення, або встановлює відразу кілька загальних полів. Діапазон допустимих значень залежить від того, чи використовує календар [м'який режим](intlcalendar.setlenient.md)

Для полів, які конфліктують, поля, які встановлюються пізніше, мають пріоритет.

Цей метод не можна викликати рівно із чотирма аргументами.

### Список параметрів

`cal`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants)полей типа дата/время. Целое число от до\*\*`IntlCalendar::FIELD_COUNT`\*\*

`value`

Нове значення вказаного поля.

`year`

Новое значение для\*\*`IntlCalendar::FIELD_YEAR`\*\*

`month`

Новое значение для\*\*`IntlCalendar::FIELD_MONTH`\*\*. Послідовність місяців відраховується з нуля, тобто. січень представлений 0, лютий – 1, …, грудень – 11, а Тринадцятий місяць (якщо в календарі) – 12.

`dayOfMonth`

Новое значение для\*\*`IntlCalendar::FIELD_DAY_OF_MONTH`\*\*

`hour`

Новое значение для\*\*`IntlCalendar::FIELD_HOUR_OF_DAY`\*\*

`minute`

Новое значение для\*\*`IntlCalendar::FIELD_MINUTE`\*\*

`second`

Новое значение для\*\*`IntlCalendar::FIELD_SECOND`\*\*

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Пример #1 Пример использования**IntlCalendar::set()\*\*\*\*

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');

// Вызовы, сделанные позже, приоритетнее
$cal = new IntlGregorianCalendar(2013, 6 /* Июль */, 1);
$cal->set(IntlCalendar::FIELD_YEAR, 2012);
$cal->set(IntlCalendar::FIELD_EXTENDED_YEAR, 2011);
var_dump(IntlDateFormatter::formatObject($cal));

$cal = new IntlGregorianCalendar(2013, 6 /* Июль */, 1);
$cal->set(IntlCalendar::FIELD_YEAR, 2012);
$cal->set(IntlCalendar::FIELD_EXTENDED_YEAR, 2011);
// Время еще не пересчитано. Если мы очистим EXTENDED_YEAR,
// будет использован предыдущий год.
$cal->clear(IntlCalendar::FIELD_EXTENDED_YEAR);
var_dump(IntlDateFormatter::formatObject($cal));
```

Результат виконання наведеного прикладу:

```
string(20) "01/07/2011, 00:00:00"
string(20) "01/07/2012, 00:00:00"
```

### Дивіться також

-   [IntlCalendar::get()](intlcalendar.get.md) \- Отримує значення поля
-   [IntlCalendar::add()](intlcalendar.add.md) \- Додає кількість (зі знаком) часу у полі
-   [IntlCalendar::roll()](intlcalendar.roll.md) \- Додає значення в поле без перенесення до важливих полів
