Перевірити, чи є код помилки ознакою збою

-   [« intlgeterrormessage](function.intl-get-error-message.html)
    
-   [Багатобайтові рядки »](book.mbstring.html)
    
-   [PHP Manual](index.html)
    
-   [Функции intl](ref.intl.html)
    
-   Перевірити, чи є код помилки ознакою збою
    

# intlісfailure

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlісfailure — Перевірити, чи є код помилки ознакою збою

### Опис

```methodsynopsis
intl_is_failure(int $errorCode): bool
```

### Список параметрів

`errorCode`

Значення, повернене функціями: [intlgeterrorcode()](function.intl-get-error-code.html) [collatorgeterrorcode()](collator.geterrorcode.html)

### Значення, що повертаються

**`true`**, якщо стався збій, і \*\*`false`\*\*якщо все успішно, або просто попередження.

### Приклади

**Приклад #1 Приклад використання **intlісfailure()****

```php
<?php
function check( $err_code )
{
    var_export( intl_is_failure( $err_code ) );
    echo "\n";
}

check( U_ZERO_ERROR );
check( U_USING_FALLBACK_WARNING );
check( U_ILLEGAL_ARGUMENT_ERROR );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
false
false
true
```

### Дивіться також

-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [collatorgeterrorcode()](collator.geterrorcode.html) - Отримує останній код помилки Collator
-   [Collator-getErrorCode()](collator.geterrorcode.html) - Отримує останній код помилки Collator