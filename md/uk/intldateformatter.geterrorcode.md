---
navigation:
  - intldateformatter.getdatetype.md: '« IntlDateFormatter::getDateType'
  - intldateformatter.geterrormessage.md: 'IntlDateFormatter::getErrorMessage »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::getErrorCode

# datefmt\_get\_error\_code

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getErrorCode -- datefmt\_get\_error\_code — Отримує код помилки останньої операції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
datefmt_get_error_code(IntlDateFormatter $formatter): int
```

Повертає код помилки останньої операції форматування.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Код помилки є одним із значень UErrorCode. Початкове значення - U\_ZERO\_ERROR.

### Приклади

**Приклад #1 Приклад использования функции**datefmt\_get\_error\_code()\*\*\*\*

```php
<?php

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = datefmt_format($fmt, 0);

printf(
    "ОШИБКА: %s (%d)\n",
    datefmt_get_error_message($fmt),
    datefmt_get_error_code($fmt)
);
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
$str = $fmt->format(0);

printf(
    "ОШИБКА: %s (%d)\n",
    $fmt->getErrorMessage(),
    $fmt->getErrorCode()
);
?>
```

Результат виконання наведеного прикладу:

```
ОШИБКА: U_ZERO_ERROR (0)
```

### Дивіться також

-   [datefmt\_get\_error\_message()](intldateformatter.geterrormessage.md) \- Отримує текст помилки останньої операції
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
