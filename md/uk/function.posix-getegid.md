---
navigation:
  - function.posix-getcwd.md: « posix\_getcwd
  - function.posix-geteuid.md: posix\_geteuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getegid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getegid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getegid - Повертає ефективний ідентифікатор групи поточного процесу EGID

### Опис

```methodsynopsis
posix_getegid(): int
```

Повертає ефективний ідентифікатор групи поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає число типу int, що відповідає ефективному ідентифікатору групи.

### Приклади

**Приклад #1 Приклад використання** posix\_getegid()\*\*\*\*

У прикладі програма виводить ефективний ідентифікатор групи процесу, змінює його за допомогою функції [posix\_setegid()](function.posix-setegid.md) і знову виводить.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Примітки

**posix\_getegid()** відрізняється від [posix\_getgid()](function.posix-getgid.md) тому, що ефективний ідентифікатор групи може бути змінений викликаним процесом, використовуючи [posix\_setegid()](function.posix-setegid.md)

### Дивіться також

-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
-   [posix\_getgid()](function.posix-getgid.md) \- Повертає дійсний ID групи поточного процесу GID
-   [posix\_setgid()](function.posix-setgid.md) \- Встановлює ідентифікатор групи для поточного процесу GID
