Повертає код помилки останньої операції

-   [« MessageFormatter::format](messageformatter.format.html)
    
-   [MessageFormatter::getErrorMessage »](messageformatter.geterrormessage.html)
    
-   [PHP Manual](index.html)
    
-   [MessageFormatter](class.messageformatter.html)
    
-   Повертає код помилки останньої операції
    

# MessageFormatter::getErrorCode

# msgfmtgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

MessageFormatter::getErrorCode -- msgfmtgeterrorcode — Повертає код помилки останньої операції

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public MessageFormatter::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
msgfmt_get_error_code(MessageFormatter $formatter): int
```

Повертає код помилки останньої операції.

### Список параметрів

`formatter`

Об'єкт [MessageFormatter](class.messageformatter.html)

### Значення, що повертаються

Код помилки є одним із значень UErrorCode. Початкове значення - UZEROERROR.

### Дивіться також

-   [msgfmtgeterrormessage()](messageformatter.geterrormessage.html) - Повертає текст помилки останньої операції
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою