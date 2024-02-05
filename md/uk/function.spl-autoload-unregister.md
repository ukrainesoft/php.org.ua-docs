---
navigation:
  - function.spl-autoload-register.md: « spl\_autoload\_register
  - function.spl-autoload.md: spl\_autoload »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload\_unregister
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload\_unregister

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload\_unregister — Скасування реєстрації функції як реалізацію методу \_\_autoload()

### Опис

```methodsynopsis
spl_autoload_unregister(callable $callback): bool
```

Видаляє функцію із черги автозавантаження. Якщо черга була активна і після видалення функції виявиться порожньою, вона буде автоматично деактивована.

Коли ця функція призводить до деактивації черги, будь-яка функція \_\_autoload, яка раніше існувала, не буде повторно активовано.

### Список параметрів

`callback`

Функція автозавантаження, реєстрацію якої потрібно зняти.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
