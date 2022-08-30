Отримує останній код помилки засобу форматування

-   [« NumberFormatter::getAttribute](numberformatter.getattribute.md)
    
-   [NumberFormatter::getErrorMessage »](numberformatter.geterrormessage.md)
    
-   [PHP Manual](index.md)
    
-   [NumberFormatter](class.numberformatter.md)
    
-   Отримує останній код помилки засобу форматування
    

# NumberFormatter::getErrorCode

# numfmtgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

NumberFormatter::getErrorCode -- numfmtgeterrorcode — Отримує останній код помилки засобу форматування

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

**Приклад #1 Приклад використання **numfmtgeterrorcode()****

```php
<?php
$fmt  = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
if(intl_is_failure(numfmt_get_error_code($fmt))) {
    report_error("Formatter error");
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
if(intl_is_failure($fmt->getErrorCode())) {
    report_error("Formatter error");
}
?>
```

### Дивіться також

-   [numfmtgeterrormessage()](numberformatter.geterrormessage.md) - Отримує останнє повідомлення про помилку засобу форматування
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою