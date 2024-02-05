---
navigation:
  - ref.intl.md: « Функції intl
  - function.intl-get-error-code.md: intl\_get\_error\_code »
  - index.md: PHP Manual
  - ref.intl.md: Функції intl
title: intl\_error\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# intl\_error\_name

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intl\_error\_name — Отримати ім'я помилки за її кодом

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

**Приклад #1 Приклад використання** intl\_error\_name()\*\*\*\*

```php
<?php
$coll     = collator_create( 'en_RU' );
$err_code = collator_get_error_code( $coll );

printf( "Символическое имя для %d - %s\n.", $err_code, intl_error_name( $err_code ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
Символическое имя для -128 - U_USING_FALLBACK_WARNING.
```

### Дивіться також

-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_get\_error\_message()](function.intl-get-error-message.md) \- Отримати опис помилки
