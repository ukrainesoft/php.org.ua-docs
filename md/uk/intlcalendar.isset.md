---
navigation:
  - intlcalendar.islenient.md: '« IntlCalendar::isLenient'
  - intlcalendar.isweekend.md: 'IntlCalendar::isWeekend »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::isSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::isSet

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::isSet — Визначає, чи встановлено поле

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::isSet(int $field): bool
```

Процедурний стиль

```methodsynopsis
intlcal_is_set(IntlCalendar $calendar, int $field): bool
```

Возвращает, установлено ли поле (в отличие от[clear](intlcalendar.clear.md)). Встановлені поля пріоритетніші за невстановлені поля та їх значення за замовчуванням при обчисленні дати та часу. Поля, встановлені пізніше за пріоритетніші полів, встановлених раніше.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.md#intlcalendar.constants)полей типа дата/время. Целое число от до\*\*`IntlCalendar::FIELD_COUNT`\*\*

### Значення, що повертаються

В случае отсутствия ошибок аргумента возвращает\*\*`true`\*\*, якщо поле встановлено.

### Приклади

Смотрите пример в описании метода[IntlCalendar::clear()](intlcalendar.clear.md)

### Дивіться також

-   [IntlCalendar::clear()](intlcalendar.clear.md) \- Очищає поле чи всі поля
-   [IntlCalendar::set()](intlcalendar.set.md) \- Встановлює поле часу або одразу кілька спільних полів
