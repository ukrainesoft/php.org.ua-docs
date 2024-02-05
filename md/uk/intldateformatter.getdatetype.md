---
navigation:
  - intldateformatter.getcalendar.md: '« IntlDateFormatter::getCalendar'
  - intldateformatter.geterrorcode.md: 'IntlDateFormatter::getErrorCode »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getDateType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getDateType

# datefmt\_get\_datetype

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getDateType -- datefmt\_get\_datetype — Отримує тип дати, який використовується IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getDateType(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_datetype(IntlDateFormatter $formatter): int|false
```

Отримує тип дати, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Значення поточного [типу дати](class.intldateformatter.md#intl.intldateformatter-constants)средства форматирования или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** datefmt\_get\_datetype()\*\*\*\*

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип даты средства форматирования : ' . datefmt_get_datetype($fmt);
echo 'Первый отформатированный вывод с типом даты ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип даты средства форматирования : ' . datefmt_get_datetype($fmt);
echo 'Второй отформатированный вывод с типом даты ' . datefmt_format($fmt, 0);

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
echo 'Тип даты средства форматирования : ' . $fmt->getDateType();
echo 'Первый отформатированный вывод с типом даты ' . $fmt->format(0);
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Теперь тип даты средства форматирования : ' . $fmt->getDateType();
echo 'Второй отформатированный вывод с типом даты ' . $fmt->format(0);

?>
```

Результат виконання наведеного прикладу:

```
Тип даты средства форматирования : 0
Первый отформатированный вывод с типом даты Wednesday, December 31, 1969 4:00:00 PM PT
Теперь тип даты средства форматирования : 2
Второй отформатированный вывод с типом даты 12/31/69 4:00:00 PM PT
```

### Дивіться також

-   [datefmt\_get\_timetype()](intldateformatter.gettimetype.md) \- Отримує тип часу, який використовується IntlDateFormatter
-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
