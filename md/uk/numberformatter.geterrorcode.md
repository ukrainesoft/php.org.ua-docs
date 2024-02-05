---
navigation:
  - numberformatter.getattribute.md: '« NumberFormatter::getAttribute'
  - numberformatter.geterrormessage.md: 'NumberFormatter::getErrorMessage »'
  - index.md: PHP Manual
  - class.numberformatter.md: NumberFormatter
title: 'NumberFormatter::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NumberFormatter::getErrorCode

# numfmt\_get\_error\_code

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getErrorCode -- numfmt\_get\_error\_code — Отримує останній код помилки засобу форматування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public NumberFormatter::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
numfmt_get_error_code(NumberFormatter $formatter): int
```

Отримує код помилки із останньої функції, виконаної засобом форматування.

### Список параметрів

`formatter`

Об'єкт [NumberFormatter](class.numberformatter.md)

### Значення, що повертаються

Повернення коду помилки з останнього виклику засобу форматування.

### Приклади

**Приклад #1 Приклад використання** numfmt\_get\_error\_code()\*\*\*\*

```php
<?php
$fmt  = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_get_error_code($fmt))) {
    report_error("Formatter error");
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

### Дивіться також

-   [numfmt\_get\_error\_message()](numberformatter.geterrormessage.md) \- Отримує останнє повідомлення про помилку засобу форматування
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
