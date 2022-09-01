---
navigation:
  - function.posix-getcwd.html: « posixgetcwd
  - function.posix-geteuid.html: posixgeteuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetegid
---
# posixgetegid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetegid - Повертає ефективний ідентифікатор групи поточного процесу EGID

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

**Приклад #1 Приклад використання **posixgetegid()****

У прикладі програма виводить ефективний ідентифікатор групи процесу, змінює його за допомогою функції [posixsetegid()](function.posix-setegid.html) і знову виводить.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Примітки

**posixgetegid()** відрізняється від [posixgetgid()](function.posix-getgid.html) тому, що ефективний ідентифікатор групи може бути змінений викликаним процесом, використовуючи [posixsetegid()](function.posix-setegid.html)

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID
-   [posixgetgid()](function.posix-getgid.html) - Повертає дійсний ID групи поточного процесу GID
-   [posixsetgid()](function.posix-setgid.html) - Встановлює ідентифікатор групи для поточного процесу GID
