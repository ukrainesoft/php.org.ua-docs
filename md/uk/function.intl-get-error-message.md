---
navigation:
  - function.intl-get-error-code.md: « intl\_get\_error\_code
  - function.intl-is-failure.md: intl\_is\_failure »
  - index.md: PHP Manual
  - ref.intl.md: Функції intl
title: intl\_get\_error\_message
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# intl\_get\_error\_message

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intl\_get\_error\_message — Отримати опис помилки

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

**Приклад #1 Приклад використання** intl\_get\_error\_message()\*\*\*\*

```php
<?php
if( Collator::getAvailableLocales() === false ) {
    show_error( intl_get_error_message() );
}
?>
```

### Дивіться також

-   [intl\_error\_name()](function.intl-error-name.md) \- Отримати ім'я помилки за її кодом
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
-   [collator\_get\_error\_message()](collator.geterrormessage.md) \- Отримує текст для останньої помилки коду Collator
-   [numfmt\_get\_error\_message()](numberformatter.geterrormessage.md) \- Отримує останнє повідомлення про помилку засобу форматування
