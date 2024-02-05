---
navigation:
  - function.session-regenerate-id.md: « session\_regenerate\_id
  - function.session-reset.md: session\_reset »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_register\_shutdown
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_register\_shutdown

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

session\_register\_shutdown - Функція завершення сесії

### Опис

```methodsynopsis
session_register_shutdown(): void
```

Реєструє функцію [session\_write\_close()](function.session-write-close.md) як функція завершення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

У разі невдалої реєстрації завершальної функції генерує помилку рівня **`E_WARNING`**
