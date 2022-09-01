---
navigation:
  - function.session-start.html: « sessionstart
  - function.session-unset.html: sessionunset »
  - index.html: PHP Manual
  - ref.session.html: Функції для роботи із сесіями
title: sessionstatus
---
# sessionstatus

(PHP 5> = 5.4.0, PHP 7, PHP 8)

sessionstatus — Повертає стан поточної сесії

### Опис

```methodsynopsis
session_status(): int
```

Функція **sessionstatus()** повертає стан поточної сесії

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

-   **`PHP_SESSION_DISABLED`**, якщо механізм сесій вимкнено.
-   **`PHP_SESSION_NONE`**, якщо механізм сесій включено, але сесія не створена.
-   **`PHP_SESSION_ACTIVE`**, якщо механізм сесій увімкнено і сесія створена.

### Дивіться також

-   [sessionstart()](function.session-start.html) - Стартує нову сесію, або відновлює існуючу
