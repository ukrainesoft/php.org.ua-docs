---
navigation:
  - intlcalendar.getactualmaximum.md: '« IntlCalendar::getActualMaximum'
  - intlcalendar.getavailablelocales.md: 'IntlCalendar::getAvailableLocales »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::getActualMinimum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::getActualMinimum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getActualMinimum — Мінімальне значення для поля з урахуванням поточного часу об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getActualMinimum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_actual_minimum(IntlCalendar $calendar, int $field): int|false
```

Повертає відносне мінімальне значення поля з урахуванням поточного часу. Точна семантика залежить від поля, але в загальному випадку це значення, яке можна було б отримати, якби встановити значення поля на [найбільший відносний мінімум](intlcalendar.getgreatestminimum.md) для поля і зменшувати його до тих пір, поки не буде досягнуто [глобальний мінімум](intlcalendar.getminimum.md) або значення поля буде обернуте навколо, в якому значення, що повертається, буде глобальним мінімумом або значенням до перенесення, відповідно.

Для григоріанського календаря це завжди те саме, що й [IntlCalendar::getMinimum()](intlcalendar.getminimum.md)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants)полей типа дата/время. Целое число от до\*\*`IntlCalendar::FIELD_COUNT`\*\*

### Значення, що повертаються

Целое число (int), представляющее значение поля или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [IntlCalendar::getMinimum()](intlcalendar.getminimum.md) \- Отримує глобальне мінімальне значення поля
-   [IntlCalendar::getGreatestMinimum()](intlcalendar.getgreatestminimum.md) \- Отримує найбільше локальне мінімальне значення поля
-   [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.md) \- Максимальне значення для поля з урахуванням поточного часу об'єкта
