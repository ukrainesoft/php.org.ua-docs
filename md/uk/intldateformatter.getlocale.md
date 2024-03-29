---
navigation:
  - intldateformatter.geterrormessage.md: '« IntlDateFormatter::getErrorMessage'
  - intldateformatter.getpattern.md: 'IntlDateFormatter::getPattern »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getLocale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getLocale

# datefmt\_get\_locale

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getLocale -- datefmt\_get\_locale — Отримує мовний стандарт, який використовується засобом форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getLocale(int $type = ULOC_ACTUAL_LOCALE): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_get_locale(IntlDateFormatter $formatter, int $type = ULOC_ACTUAL_LOCALE): string|false
```

Отримує мовний стандарт, який використовується засобом форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`type`

Ви можете вибирати між коректним та поточним мовним стандартом (\*\*`Locale::VALID_LOCALE`** і **`Locale::ACTUAL_LOCALE`\*\*відповідно). За промовчанням використовується поточний мовний стандарт.

### Значення, що повертаються

Мовний стандарт засобу форматування або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** datefmt\_get\_locale()\*\*\*\*

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Языковой стандарт средства форматирования : ' . datefmt_get_locale($fmt);
echo 'Первый отформатированный вывод ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Языковой стандарт средства форматирования : ' . datefmt_get_locale($fmt);
echo 'Второй отформатированный вывод ' . datefmt_format($fmt, 0);

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
echo 'Языковой стандарт средства форматирования : ' . $fmt->getLocale();
echo 'Первый отформатированный вывод ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Языковой стандарт средства форматирования : ' . $fmt->getLocale();
echo 'Второй отформатированный вывод ' . $fmt->format(0);

?>
```

Результат виконання наведеного прикладу:

```
Языковой стандарт средства форматирования : en
Первый отформатированный вывод Wednesday, December 31, 1969 4:00:00 PM PT
Языковой стандарт средства форматирования : de
Второй отформатированный вывод Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
```

### Дивіться також

-   [datefmt\_create()](intldateformatter.create.md) \- Створює засіб форматування дати
