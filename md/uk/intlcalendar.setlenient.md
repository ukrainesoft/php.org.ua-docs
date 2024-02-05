---
navigation:
  - intlcalendar.setfirstdayofweek.md: '« IntlCalendar::setFirstDayOfWeek'
  - intlcalendar.setminimaldaysinfirstweek.md: 'IntlCalendar::setMinimalDaysInFirstWeek »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setLenient'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setLenient

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setLenient — Встановлює, чи інтерпретація дати/часу повинна бути м'якою.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setLenient(bool $lenient): true
```

Процедурний стиль

```methodsynopsis
intlcal_set_lenient(IntlCalendar $calendar, bool $lenient): true
```

Визначає, чи календар "м'яким" режимом. У такому режимі приймаються деякі з значень, що виходять за кордон для деяких полів, поведінка аналогічна поведінці [IntlCalendar::add()](intlcalendar.add.md) (тобто значення переноситься щоразу на більш важливі поля). Якщо м'який режим вимкнено, такі значення викликатимуть помилку.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`lenient`

Используйте\*\*`true`**для активации мягкого режима;**`false`\*\* для вимикання.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

Смотрите Приклад в описании метода[IntlCalendar::isLenient()](intlcalendar.islenient.md)
