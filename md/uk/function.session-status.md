---
navigation:
  - function.session-start.md: « session\_start
  - function.session-unset.md: session\_unset »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_status

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

session\_status — Повертає стан поточної сесії

### Опис

```methodsynopsis
session_status(): int
```

Функция**session\_status()** повертає стан поточної сесії

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

-   **`PHP_SESSION_DISABLED`**, якщо механізм сесій вимкнено.
-   **`PHP_SESSION_NONE`**, якщо механізм сесій включено, але сесія не створена.
-   **`PHP_SESSION_ACTIVE`**, якщо механізм сесій увімкнено і сесія створена.

### Дивіться також

-   [session\_start()](function.session-start.md) \- Стартує нову сесію, або відновлює існуючу
