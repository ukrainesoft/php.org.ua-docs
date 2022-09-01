---
navigation:
  - intlcalendar.islenient.md: '« IntlCalendar::isLenient'
  - intlcalendar.isweekend.md: 'IntlCalendar::isWeekend »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::isSet'
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

Повертає, чи встановлено поле (на відміну від [clear](intlcalendar.clear.md)). Встановлені поля пріоритетніші за невстановлені поля та їх значення за замовчуванням при обчисленні дати та часу. Поля, встановлені пізніше за пріоритетніші полів, встановлених раніше.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

У разі відсутності помилок аргумент повертає **`true`**, якщо поле встановлено.

### Приклади

Дивіться приклад в описі методу [IntlCalendar::clear()](intlcalendar.clear.md)

### Дивіться також

-   [IntlCalendar::clear()](intlcalendar.clear.md) - Очищає поле чи всі поля
-   [IntlCalendar::set()](intlcalendar.set.md) - Встановлює поле часу або одразу кілька спільних полів
