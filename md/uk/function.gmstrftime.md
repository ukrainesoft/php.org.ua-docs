---
navigation:
  - function.gmmktime.md: « gmmktime
  - function.idate.md: idate »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: gmstrftime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmstrftime

(PHP 4, PHP 5, PHP 7, PHP 8)

gmstrftime — Форматує дату/час за Грінвічем з урахуванням поточної локалі

**Увага**

Функція оголошена *застарілої* у PHP 8.1.0. Покладатися на цю функцію не рекомендується.

Є такі альтернативи:

-   [gmdate()](function.gmdate.md)
-   [IntlDateFormatter::format()](intldateformatter.format.md)

### Опис

```methodsynopsis
gmstrftime(string $format, ?int $timestamp = null): string|false
```

Ця функція ідентична функції [strftime()](function.strftime.md) за винятком того, що повертає час за Гринвічем (GMT). Наприклад, при запуску на системі, де встановлено Eastern Standard Time (GMT-0500), перший рядок з прикладу нижче виведе "Dec 31 1998 20:00:00", тоді як другий - "Jan 01 1999 01:00:00".

**Увага**

Функція залежить від інформації про локаль операційної системи, яка може бути несумісна один з одним або взагалі бути відсутнім. Замість цієї функції використовуйте метод [IntlDateFormatter::format()](intldateformatter.format.md)

### Список параметрів

`format`

Смотрите описание функции[strftime()](function.strftime.md)

`timestamp`

Необов'язковий параметр `timestamp` — це ціла (int) мітка часу, за умовчанням рівна поточному місцевому часу, якщо параметр `timestamp` не вказано або дорівнює \*\*`null`\*\*Говоря по другому, значение по умолчанию равно результату функции[time()](function.time.md)

### Значення, що повертаються

Повертає рядок, відформатований згідно з вказаним форматом та з використанням тимчасової мітки з параметра `timestamp` або поточного локального часу, якщо тимчасова мітка не була вказана. Назви місяців, днів тижня та інших мовозалежних рядків будуть показані з урахуванням налаштувань поточної локалі, встановлених за допомогою функції [setlocale()](function.setlocale.md). У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timestamp` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования функции**gmstrftime()\*\*\*\*

```php
<?php
setlocale(LC_TIME, 'en_US');
echo strftime("%b %d %Y %H:%M:%S", mktime(20, 0, 0, 12, 31, 98)) . "\n";
echo gmstrftime("%b %d %Y %H:%M:%S", mktime(20, 0, 0, 12, 31, 98)) . "\n";
?>
```

### Дивіться також

-   [IntlDateFormatter::format()](intldateformatter.format.md) \- Форматує значення дати/часу у вигляді рядка
-   [DateTimeInterface::format()](datetime.format.md) \- Повертає дату, відформатовану згідно з переданим форматом
-   [strftime()](function.strftime.md) \- Форматує поточну дату/час з урахуванням поточних налаштувань локалі
