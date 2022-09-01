---
navigation:
  - function.session-regenerate-id.html: « sessionregenerateід
  - function.session-reset.html: sessionreset »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionregistershutdown
---
# sessionregistershutdown

(PHP 5> = 5.4.0, PHP 7, PHP 8)

sessionregistershutdown - Функція завершення сесії

### Опис

```methodsynopsis
session_register_shutdown(): void
```

Реєструє функцію [sessionwriteclose()](function.session-write-close.html) як функція завершення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

При невдалій реєстрації завершальної функції генерує помилку рівня **`E_WARNING`**
