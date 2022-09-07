---
navigation:
  - numberformatter.geterrorcode.md: '« NumberFormatter::getErrorCode'
  - numberformatter.getlocale.md: 'NumberFormatter::getLocale »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getErrorMessage'
---
# NumberFormatter::getErrorMessage

# numfmtgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getErrorMessage -- numfmtgeterrormessage — Отримує останнє повідомлення про помилку засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getErrorMessage(): string
```

Процедурний стиль

```methodsynopsis
numfmt_get_error_message(NumberFormatter $formatter): string
```

Отримує повідомлення про помилку від останньої функції, виконаної засобом форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

### Значення, що повертаються

Повертає повідомлення про помилку з останнього виклику засобу форматування.

### Приклади

**Приклад #1 Приклад використання **numfmtgeterrormessage()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

### Дивіться також

-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
-   [intlgeterrorcode()](function.intl-get-error-code.md) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.md) - Перевірити, чи є код помилки ознакою збою
