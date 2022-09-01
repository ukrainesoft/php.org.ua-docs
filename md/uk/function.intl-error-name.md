---
navigation:
  - ref.intl.md: « Функции intl
  - function.intl-get-error-code.html: intlgeterrorcode »
  - index.md: PHP Manual
  - ref.intl.md: Функции intl
title: intlerrorname
---
# intlerrorname

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlerrorname — Отримати ім'я помилки за її кодом

### Опис

```methodsynopsis
intl_error_name(int $errorCode): string
```

Повертає ім'я помилки ICU.

### Список параметрів

`errorCode`

Код помилки ICU.

### Значення, що повертаються

Повертається рядок матиме ім'я аналогічне відповідній константі.

### Приклади

**Приклад #1 Приклад використання **intlerrorname()****

```php
<?php
$coll     = collator_create( 'en_RU' );
$err_code = collator_get_error_code( $coll );

printf( "Символическое имя для %d - %s\n.", $err_code, intl_error_name( $err_code ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Символическое имя для -128 - U_USING_FALLBACK_WARNING.
```

### Дивіться також

-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlgeterrormessage()](function.intl-get-error-message.html) - Отримати опис помилки
