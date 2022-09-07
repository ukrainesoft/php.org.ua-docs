---
navigation:
  - function.posix-setrlimit.md: « posixsetrlimit
  - function.posix-setuid.md: posixsetuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixsetsid
---
# posixsetsid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixsetsid - Робить поточний процес лідером сесії

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
