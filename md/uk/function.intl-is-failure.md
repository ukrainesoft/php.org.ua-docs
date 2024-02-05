---
navigation:
  - function.intl-get-error-message.md: « intl\_get\_error\_message
  - book.mbstring.md: Багатобайтові рядки »
  - index.md: PHP Manual
  - ref.intl.md: Функції intl
title: intl\_is\_failure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# intl\_is\_failure

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intl\_is\_failure — Перевірити, чи є код помилки ознакою збою

### Опис

```methodsynopsis
intl_is_failure(int $errorCode): bool
```

### Список параметрів

`errorCode`

Значення, повернене функціями: [intl\_get\_error\_code()](function.intl-get-error-code.md) [collator\_get\_error\_code()](collator.geterrorcode.md)

### Значення, що повертаються

**`true`**, якщо стався збій, і \*\*`false`\*\*якщо все успішно, або просто попередження.

### Приклади

**Пример #1 Пример использования**intl\_is\_failure()\*\*\*\*

```php
<?php
function check( $err_code )
{
    var_export( intl_is_failure( $err_code ) );
    echo "\n";
}

check( U_ZERO_ERROR );
check( U_USING_FALLBACK_WARNING );
check( U_ILLEGAL_ARGUMENT_ERROR );
?>
```

Висновок наведеного прикладу буде схожим на:

```
false
false
true
```

### Дивіться також

-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [collator\_get\_error\_code()](collator.geterrorcode.md) \- Отримує останній код помилки Collator
-   [Collator-getErrorCode()](collator.geterrorcode.md) \- Отримує останній код помилки Collator
