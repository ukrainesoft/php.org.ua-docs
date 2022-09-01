---
navigation:
  - ref.misc.md: « Різні функції
  - function.connection-status.html: connectionstatus »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: connectionaborted
---
# connectionaborted

(PHP 4, PHP 5, PHP 7, PHP 8)

connectionaborted — Перевірити, чи клієнт вимкнено

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

-   [connectionstatus()](function.connection-status.md) - Повертає статус з'єднання у бітах
-   [ignoreuserabort()](function.ignore-user-abort.md) - Встановити, чи має відключення клієнта переривати виконання скрипту
-   Дивіться [Управление подключениями](features.connection-handling.md) для отримання повного опису управління підключення PHP.
