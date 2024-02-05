---
navigation:
  - function.intl-error-name.md: « intl\_error\_name
  - function.intl-get-error-message.md: intl\_get\_error\_message »
  - index.md: PHP Manual
  - ref.intl.md: Функції intl
title: intl\_get\_error\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# intl\_get\_error\_code

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

intl\_get\_error\_code — Отримати код останньої помилки

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

**Пример #1 Пример использования**intl\_get\_error\_code()\*\*\*\*

```php
<?php
$coll = collator_create( '<bad_param>' );
if( !$coll ) {
    handle_error( intl_get_error_code() );
}
?>
```

### Дивіться також

-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
-   [intl\_error\_name()](function.intl-error-name.md) \- Отримати ім'я помилки за її кодом
-   [intl\_get\_error\_message()](function.intl-get-error-message.md) \- Отримати опис помилки
-   [collator\_get\_error\_code()](collator.geterrorcode.md) \- Отримує останній код помилки Collator
-   [numfmt\_get\_error\_code()](numberformatter.geterrorcode.md) \- Отримує останній код помилки засобу форматування
