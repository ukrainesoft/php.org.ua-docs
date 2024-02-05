---
navigation:
  - intldateformatter.gettimetype.md: '« IntlDateFormatter::getTimeType'
  - intldateformatter.getcalendarobject.md: 'IntlDateFormatter::getCalendarObject »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getTimeZoneId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getTimeZoneId

# datefmt\_get\_timezone\_id

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getTimeZoneId -- datefmt\_get\_timezone\_id — Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getTimeZoneId(): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_timezone_id(IntlDateFormatter $formatter): string|false
```

Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Рядок ідентифікатора часового поясу, який використовується цим засобом форматування або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**datefmt\_get\_timezone\_id()\*\*\*\*

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id средства форматирования: ' . datefmt_get_timezone_id($fmt) . "\n";
datefmt_set_timezone($fmt, 'Europe/Madrid');
echo 'Теперь timezone_id средства форматирования: ' . datefmt_get_timezone_id($fmt);

?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'timezone_id средства форматирования: ' . $fmt->getTimezoneId() . "\n";
$fmt->setTimezone('Europe/Madrid');
echo 'Теперь timezone_id средства форматирования: ' . $fmt->getTimezoneId();

?>
```

Результат виконання наведеного прикладу:

```
timezone_id средства форматирования: America/Los_Angeles
Теперь timezone_id средства форматирования: Europe/Madrid
```

### Дивіться також

-   [datefmt\_set\_timezone()](intldateformatter.settimezone.md) \- Встановлює часовий пояс засобу форматування
-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
