Отримує останнє повідомлення про помилку засобу форматування

-   [« NumberFormatter::getErrorCode](numberformatter.geterrorcode.html)
    
-   [NumberFormatter::getLocale »](numberformatter.getlocale.html)
    
-   [PHP Manual](index.html)
    
-   [NumberFormatter](class.numberformatter.html)
    
-   Отримує останнє повідомлення про помилку засобу форматування
    

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

Об'єкт [NumberFormatter](class.numberformatter.html)

### Значення, що повертаються

Повертає повідомлення про помилку з останнього виклику засобу форматування.

### Приклади

**Приклад #1 Приклад використання **numfmtgeterrormessage()****

```php
<?php
$fmt = numfmt_create( 'de_DE', NumberFormatter::DECIMAL );
$data = numfmt_format($fmt, 1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new NumberFormatter( 'de_DE', NumberFormatter::DECIMAL );
$fmt->format(1234567.891234567890000);
var_dump(numfmt_get_error_message($fmt));
?>
```

### Дивіться також

-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.html) - Отримує останній код помилки засобу форматування
-   [intl\_get\_error\_code()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою