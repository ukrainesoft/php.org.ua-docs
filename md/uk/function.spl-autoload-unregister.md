---
navigation:
  - function.spl-autoload-register.html: « splautoloadregister
  - function.spl-autoload.html: splautoload »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: splautoloadunregister
---
# splautoloadunregister

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadunregister — Скасування реєстрації функції як реалізацію методу autoload()

### Опис

```methodsynopsis
spl_autoload_unregister(callable $callback): bool
```

Видаляє функцію із черги автозавантаження. Якщо черга була активна і після видалення функції виявиться порожньою, вона буде автоматично деактивована.

Коли ця функція призводить до деактивації черги, будь-яка функція autoload, яка раніше існувала, не буде повторно активовано.

### Список параметрів

`callback`

Функція автозавантаження, реєстрацію якої потрібно зняти.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
