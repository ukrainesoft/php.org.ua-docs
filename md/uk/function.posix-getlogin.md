---
navigation:
  - function.posix-getgroups.md: « posix\_getgroups
  - function.posix-getpgid.md: posix\_getpgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getlogin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getlogin

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getlogin — Повертає логін власника процесу

### Опис

```methodsynopsis
posix_getlogin(): string|false
```

Повертає логін користувача, який є власником цього процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає логін користувача як змінну типу string або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_getlogin()\*\*\*\*

```php
<?php
echo posix_getlogin(); //apache
?>
```

### Дивіться також

-   [posix\_getpwnam()](function.posix-getpwnam.md) \- Повертає інформацію про користувача на його ім'я
-   POSIX керівництво GETLOGIN(3)
