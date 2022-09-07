---
navigation:
  - intldateformatter.getdatetype.md: '« IntlDateFormatter::getDateType'
  - intldateformatter.geterrormessage.md: 'IntlDateFormatter::getErrorMessage »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::getErrorCode'
---
# IntlDateFormatter::getErrorCode

# datefmtgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getErrorCode -- datefmtgeterrorcode — Отримує код помилки останньої операції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
datefmt_get_error_code(IntlDateFormatter $formatter): int
```

Отримує код помилки останньої операції. Повертає код помилки останньої операції форматування числа.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Код помилки є одним із значень UErrorCode. Початкове значення - UZEROERROR.

### Приклади

**Приклад #1 Приклад використання **datefmtgeterrorcode()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = datefmt_format($fmt);
if (!$str) {
    printf(
        "ОШИБКА: %s (%d)\n",
        datefmt_get_error_message($fmt),
        datefmt_get_error_code($fmt)
    );
}
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
$str = $fmt->format();
if (!$str) {
    printf(
        "ОШИБКА: %s (%d)\n",
        $fmt->getErrorMessage(),
        $fmt->getErrorCode()
    );
}
?>
```

Результат виконання цього прикладу:

```
ОШИБКА: U_ZERO_ERROR (0)
```

### Дивіться також

-   [datefmtgeterrormessage()](intldateformatter.geterrormessage.md) - Отримує текст помилки останньої операції
-   [intlgeterrorcode()](function.intl-get-error-code.md) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.md) - Перевірити, чи є код помилки ознакою збою
