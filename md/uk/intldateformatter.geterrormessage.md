Отримує текст помилки останньої операції

-   [« IntlDateFormatter::getErrorCode](intldateformatter.geterrorcode.html)
    
-   [IntlDateFormatter::getLocale »](intldateformatter.getlocale.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Отримує текст помилки останньої операції
    

# IntlDateFormatter::getErrorMessage

# datefmtgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::getErrorMessage -- datefmtgeterrormessage — Отримує текст помилки останньої операції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::getErrorMessage(): string
```

Процедурний стиль

```methodsynopsis
datefmt_get_error_message(IntlDateFormatter $formatter): string
```

Отримує помилку останньої операції.

### Список параметрів

`formatter`

Ресурс засобу форматування.

### Значення, що повертаються

Опис останньої помилки.

### Приклади

**Приклад #1 Приклад використання **datefmtgeterrormessage()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = datefmt_format($fmt);
if (!$str) {
    printf(
        "ОШИБКА: %s (%d)\n",
        datefmt_get_error_message($fmt),
        datefmt_get_error_code($fmt)
    );
}
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
$str = $fmt->format();
if(!$str) {
    printf(
        "ОШИБКА: %s (%d)\n",
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

-   [datefmt\_get\_error\_code()](intldateformatter.geterrorcode.html) - Отримує код помилки останньої операції
-   [intl\_get\_error\_code()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою