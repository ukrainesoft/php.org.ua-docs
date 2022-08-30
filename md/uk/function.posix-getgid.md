Повертає дійсний ID групи поточного процесу GID

-   [« posixgeteuid](function.posix-geteuid.html)
    
-   [posixgetgrgid »](function.posix-getgrgid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає дійсний ID групи поточного процесу GID
    

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

-   [posixgetgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID
-   [posixgetegid()](function.posix-getegid.html) - Повертає ефективний ідентифікатор групи поточного процесу EGID
-   [posixsetgid()](function.posix-setgid.html) - Встановлює ідентифікатор групи для поточного процесу GID
-   POSIX керівництво GETGID(2)