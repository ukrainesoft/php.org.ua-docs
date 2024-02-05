---
navigation:
  - ref.misc.md: « Різні функції
  - function.connection-status.md: connection\_status »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: connection\_aborted
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# connection\_aborted

(PHP 4, PHP 5, PHP 7, PHP 8)

connection\_aborted — Перевірити, чи клієнт вимкнено

### Опис

```methodsynopsis
connection_aborted(): int
```

Перевіряє, чи клієнт вимкнено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 1, якщо клієнт вимкнено, 0 інакше.

### Дивіться також

-   [connection\_status()](function.connection-status.md) \- Повертає бітове поле стану з'єднання
-   [ignore\_user\_abort()](function.ignore-user-abort.md) \- Встановити, чи має відключення клієнта переривати виконання скрипту
-   Смотрите[Управління підключеннями](features.connection-handling.md)для отримання повного опису управління підключення PHP.
