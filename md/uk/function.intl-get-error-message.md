---
navigation:
  - function.intl-get-error-code.html: « intlgeterrorcode
  - function.intl-is-failure.html: intlісfailure »
  - index.md: PHP Manual
  - ref.intl.md: Функции intl
title: intlgeterrormessage
---
# intlgeterrormessage

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlgeterrormessage — Отримати опис помилки

### Опис

```methodsynopsis
intl_get_error_message(): string
```

Отримати опис останньої помилки у функціях ICU.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Опис останньої помилки у функціях ICU.

### Приклади

**Приклад #1 Приклад використання **intlgeterrormessage()****

```php
<?php
if( Collator::getAvailableLocales() === false ) {
    show_error( intl_get_error_message() );
}
?>
```

### Дивіться також

-   [intlerrorname()](function.intl-error-name.html) - Отримати ім'я помилки за її кодом
-   [intlgeterrorcode()](function.intl-get-error-code.html) - Отримати код останньої помилки
-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою
-   [collatorgeterrormessage()](collator.geterrormessage.md) - Отримує текст для останньої помилки коду Collator
-   [numfmtgeterrormessage()](numberformatter.geterrormessage.md) - Отримує останнє повідомлення про помилку засобу форматування
