---
navigation:
  - function.connection-aborted.html: « connectionaborted
  - function.constant.md: constant »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: connectionstatus
---
# connectionstatus

(PHP 4, PHP 5, PHP 7, PHP 8)

connectionstatus — Повертає статус з'єднання в бітах

### Опис

```methodsynopsis
connection_status(): int
```

Набуває статусу з'єднання в бітах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає статус з'єднання в бітах, який можна використовувати у константах `CONNECTION_XXX` визначення статусу з'єднання.

### Дивіться також

-   [connectionaborted()](function.connection-aborted.html) - Перевірити, чи клієнт вимкнено
-   [ignoreuserabort()](function.ignore-user-abort.html) - Встановити, чи має відключення клієнта переривати виконання скрипту
-   Дивіться [Управление соединением](features.connection-handling.html) для повної інформації про управління з'єднанням PHP.
