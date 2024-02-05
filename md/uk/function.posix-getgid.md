---
navigation:
  - function.posix-geteuid.md: « posix\_geteuid
  - function.posix-getgrgid.md: posix\_getgrgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getgid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getgid — Повертає дійсний ID групи поточного процесу GID

### Опис

```methodsynopsis
posix_getgid(): int
```

Повертає число, яке відповідає дійсному ID групи поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає int, що відповідає дійсному ID групи поточного процесу.

### Приклади

**Пример #1 Пример использования**posix\_getgid()\*\*\*\*

У прикладі виводиться дійсний ідентифікатор групи процесу до і після того, як ефективний ідентифікатор групи процесу був змінений.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Дивіться також

-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
-   [posix\_getegid()](function.posix-getegid.md) \- Повертає ефективний ідентифікатор групи поточного процесу EGID
-   [posix\_setgid()](function.posix-setgid.md) \- Встановлює ідентифікатор групи для поточного процесу GID
-   POSIX керівництво GETGID(2)
