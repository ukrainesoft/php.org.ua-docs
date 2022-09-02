---
navigation:
  - function.posix-geteuid.md: « posixgeteuid
  - function.posix-getgrgid.md: posixgetgrgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetgid
---
# posixgetgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetgid — Повертає дійсний ID групи поточного процесу GID

### Опис

```methodsynopsis
posix_getgid(): int
```

Повертає число, що відповідає дійсному ID групи поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає int, що відповідає дійсному ID групи поточного процесу.

### Приклади

**Приклад #1 Приклад використання **posixgetgid()****

У прикладі виводиться дійсний ідентифікатор групи процесу до і після того, як ефективний ідентифікатор групи процесу був змінений.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
-   [posixgetegid()](function.posix-getegid.md) - Повертає ефективний ідентифікатор групи поточного процесу EGID
-   [posixsetgid()](function.posix-setgid.md) - Встановлює ідентифікатор групи для поточного процесу GID
-   POSIX керівництво GETGID(2)
