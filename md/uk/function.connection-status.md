---
navigation:
  - function.connection-aborted.md: « connection\_aborted
  - function.constant.md: constant »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: connection\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# connection\_status

(PHP 4, PHP 5, PHP 7, PHP 8)

connection\_status — Повертає бітове поле стану з'єднання.

### Опис

```methodsynopsis
connection_status(): int
```

Отримує бітове поле стану з'єднання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітове поле стану з'єднання, який можна використовувати з константами [**`CONNECTION_*`**](misc.constants.md)для определения состояния соединения.

### Дивіться також

-   [connection\_aborted()](function.connection-aborted.md) \- Перевірити, чи клієнт вимкнено
-   [ignore\_user\_abort()](function.ignore-user-abort.md) \- Встановити, чи має відключення клієнта переривати виконання скрипту
-   Детально про керування з'єднаннями в PHP розказано у розділі «[Управління з'єднанням](features.connection-handling.md)».
