---
navigation:
  - function.gettimeofday.md: « gettimeofday
  - function.gmmktime.md: gmmktime »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: gmdate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmdate

(PHP 4, PHP 5, PHP 7, PHP 8)

gmdate — Форматує дату/час за Грінвічем

### Опис

```methodsynopsis
gmdate(string $format, ?int $timestamp = null): string
```

Ця функція ідентична функції [date()](function.date.md) за винятком того, що повертає час за Гринвічем (GMT).

### Список параметрів

`format`

Формат дати типу рядок (string). Дивіться параметри форматування для функції [date()](function.date.md)

`timestamp`

Необов'язковий параметр `timestamp` — це ціла (int) мітка часу, за умовчанням рівна поточному місцевому часу, якщо параметр `timestamp` не вказано або дорівнює \*\*`null`\*\*Говоря по другому, значение по умолчанию равно результату функции[time()](function.time.md)

### Значення, що повертаються

Повертає рядок із форматованою датою.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timestamp` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**gmdate()\*\*\*\*

Наприклад, у Фінляндії (GMT +0200), перший рядок у наступному прикладі виведе "Jan 01 1998 00:00:00", а другий - "Dec 31 1997 22:00:00".

```php
<?php
echo date("M d Y H:i:s", mktime(0, 0, 0, 1, 1, 1998));
echo gmdate("M d Y H:i:s", mktime(0, 0, 0, 1, 1, 1998));
?>
```

### Дивіться також

-   [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md) \- Повертає новий об'єкт DateTimeImmutable
-   [DateTimeInterface::format()](datetime.format.md) \- Повертає дату, відформатовану згідно з переданим форматом
-   [date()](function.date.md) \- Форматує тимчасову мітку Unix
-   [mktime()](function.mktime.md) \- Повертає позначку часу Unix для заданої дати
-   [gmmktime()](function.gmmktime.md) \- Повертає локальну мітку часу Unix для часу за Грінвічем
-   [IntlDateFormatter::format()](intldateformatter.format.md) \- Форматує значення дати/часу у вигляді рядка
