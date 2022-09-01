---
navigation:
  - function.intl-error-name.html: « intlerrorname
  - function.intl-get-error-message.html: intlgeterrormessage »
  - index.md: PHP Manual
  - ref.intl.md: Функции intl
title: intlgeterrorcode
---
# intlgeterrorcode

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intlgeterrorcode — Отримати код останньої помилки

### Опис

```methodsynopsis
intl_get_error_code(): int
```

Корисно для обробки помилок статичних методів, коли немає об'єкта для вилучення помилки з нього.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Код помилки, повернутий останнім викликом функції API.

### Приклади

**Приклад #1 Приклад використання **intlgeterrorcode()****

```php
<?php
$coll = collator_create( '<bad_param>' );
if( !$coll ) {
    handle_error( intl_get_error_code() );
}
?>
```

### Дивіться також

-   [intlісfailure()](function.intl-is-failure.html) - Перевірити, чи є код помилки ознакою збою
-   [intlerrorname()](function.intl-error-name.html) - Отримати ім'я помилки за її кодом
-   [intlgeterrormessage()](function.intl-get-error-message.html) - Отримати опис помилки
-   [collatorgeterrorcode()](collator.geterrorcode.md) - Отримує останній код помилки Collator
-   [numfmtgeterrorcode()](numberformatter.geterrorcode.md) - Отримує останній код помилки засобу форматування
