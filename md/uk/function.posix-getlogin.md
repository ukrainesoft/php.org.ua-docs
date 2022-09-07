---
navigation:
  - function.posix-getgroups.md: « posixgetgroups
  - function.posix-getpgid.md: posixgetpgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetlogin
---
# posixgetlogin

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetlogin — Повертає логін власника процесу

### Опис

```methodsynopsis
posix_getlogin(): string|false
```

Повертає логін користувача, який є власником цього процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає логін користувача як змінну типу string або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixgetlogin()****

```php
<?php
echo posix_getlogin(); //apache
?>
```

### Дивіться також

-   [posixgetpwnam()](function.posix-getpwnam.md) - Повертає інформацію про користувача на його ім'я
-   POSIX керівництво GETLOGIN(3)
