---
navigation:
  - function.posix-setrlimit.md: « posix\_setrlimit
  - function.posix-setuid.md: posix\_setuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setsid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setsid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_setsid - Робить поточний процес лідером сесії

### Опис

```methodsynopsis
posix_setsid(): int
```

Робить поточний процес лідером сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор сесії або -1 у разі помилки.

### Дивіться також

-   Стандарт POSIX.1 посібник з setsid(2) у POSIX сумісних системах для отримання більш повної інформації про групи процесів та управління завданнями.
