---
navigation:
  - intldateformatter.formatobject.md: '« IntlDateFormatter::formatObject'
  - intldateformatter.getdatetype.md: 'IntlDateFormatter::getDateType »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getCalendar'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getCalendar

# datefmt\_get\_calendar

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getCalendar -- datefmt\_get\_calendar — Отримує тип календаря для об'єкта IntlDateFormatter

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getCalendar(): int|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_calendar(IntlDateFormatter $formatter): int|false
```

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Повертає [тип календаря](class.intldateformatter.md#intl.intldateformatter-constants.calendartypes)для сервиса форматирования. Либо\*\*`IntlDateFormatter::TRADITIONAL`**, либо**`IntlDateFormatter::GREGORIAN`\*\*. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання функції** datefmt\_get\_calendar()\*\*\*\*

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
datefmt_set_calendar($fmt, IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . datefmt_get_calendar($fmt);
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
echo 'Тип календаря средства форматирования : ' . $fmt->getCalendar();
$fmt->setCalendar(IntlDateFormatter::TRADITIONAL);
echo 'Теперь тип календаря средства форматирования : ' . $fmt->getCalendar();

?>
```

**Приклад #3 Приклад обробки неправильного значення мовного стандарту**

```php
<?php
try {
    $fmt = new IntlDateFormatter(
        'invalid_locale',
        IntlDateFormatter::FULL,
        IntlDateFormatter::FULL,
        'dunno',
        IntlDateFormatter::GREGORIAN,
    );
    $cal = $fmt->getCalendar();
} catch (\Error $e) {
    // ...
}
?>
```

**Приклад #4 Приклад обробки неприпустимого мовного стандарту**

```php
<?php
try {
    $fmt = new IntlDateFormatter(
        'invalid_locale',
        IntlDateFormatter::FULL,
        IntlDateFormatter::FULL,
        'dunno',
        IntlDateFormatter::GREGORIAN,
    );
    $cal = $fmt->getCalendar();
} catch (\Error $e) {
    // ...
}
?>
```

Результат виконання наведеного прикладу:

```
Тип календаря средства форматирования : 1
Теперь тип календаря средства форматирования : 0
```

### Дивіться також

-   [datefmt\_get\_calendar\_object()](intldateformatter.getcalendarobject.md) \- Отримує копію об'єкта календаря засобу форматування
-   [datefmt\_set\_calendar()](intldateformatter.setcalendar.md) \- Встановлює тип календаря, який використовується засобом форматування
-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
