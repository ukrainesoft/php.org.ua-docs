---
navigation:
  - intlcalendar.setrepeatedwalltimeoption.md: '« IntlCalendar::setRepeatedWallTimeOption'
  - intlcalendar.settime.md: 'IntlCalendar::setTime »'
  - index.md: PHP Manual
  - class.intlcalendar.md: IntlCalendar
title: 'IntlCalendar::setSkippedWallTimeOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlCalendar::setSkippedWallTimeOption

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setSkippedWallTimeOption — Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setSkippedWallTimeOption(int $option): true
```

Процедурний стиль

```methodsynopsis
intlcal_set_skipped_wall_time_option(IntlCalendar $calendar, int $option): true
```

Встановлює поточну стратегію для роботи з часом процесора, що пропускається щоразу, коли годинник переводиться на літній час. Значення за замовчуванням - **`IntlCalendar::WALLTIME_LAST`** (Момент, коли час процесора на годину більше). Альтернативні значення: **`IntlCalendar::WALLTIME_FIRST`**(момент, когда время процессора на один час меньше) и\*\*`IntlCalendar::WALLTIME_NEXT_VALID`\*\*(момент, когда начинается летнее время).

Впливає лише на момент, поданий календарем (як повідомляє [IntlCalendar::getTime()](intlcalendar.gettime.md)), значення поля не буде переписано відповідним чином.

Щоб ця опція мала якийсь ефект, календар має бути в [м'якому](intlcalendar.setlenient.md) режимі, в іншому випадку спроба встановити неіснуючий час викликає помилку. error.

Для цієї функції потрібний ICU 4.9 або новіший.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`option`

Одна из констант:**`IntlCalendar::WALLTIME_FIRST`** **`IntlCalendar::WALLTIME_LAST`**или**`IntlCalendar::WALLTIME_NEXT_VALID`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

Дивіться приклади у описі функції [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md)

### Дивіться також

-   [intlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) \- отримує поведінку для обробки пропущеного часу процесора
-   [intlCalendar::setRepeatedWallTimeOption()](intlcalendar.setrepeatedwalltimeoption.md) \- Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу
-   [intlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.md) \- Отримує поведінку для обробки повторюваного часу процесора
