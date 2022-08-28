Повертає ефективний ідентифікатор групи поточного процесу EGID

-   [« posix\_getcwd](function.posix-getcwd.html)
    
-   [posix\_geteuid »](function.posix-geteuid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає ефективний ідентифікатор групи поточного процесу EGID
    

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

У прикладі програма виводить ефективний ідентифікатор групи процесу, змінює його за допомогою функції [posix\_setegid()](function.posix-setegid.html) і знову виводить.

```php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### Примітки

**posixgetegid()** відрізняється від [posix\_getgid()](function.posix-getgid.html) тому, що ефективний ідентифікатор групи може бути змінений викликаним процесом, використовуючи [posix\_setegid()](function.posix-setegid.html)

### Дивіться також

-   [posix\_getgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID
-   [posix\_getgid()](function.posix-getgid.html) - Повертає дійсний ID групи поточного процесу GID
-   [posix\_setgid()](function.posix-setgid.html) - Встановлює ідентифікатор групи для поточного процесу GID