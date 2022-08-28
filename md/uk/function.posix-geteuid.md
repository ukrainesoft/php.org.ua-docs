Повертає ефективний ідентифікатор користувача поточного процесу EUID

-   [« posix\_getegid](function.posix-getegid.html)
    
-   [posix\_getgid »](function.posix-getgid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає ефективний ідентифікатор користувача поточного процесу EUID
    

# posixgeteuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgeteuid — Повертає ефективний ідентифікатор користувача поточного процесу EUID

### Опис

```methodsynopsis
posix_geteuid(): int
```

Повертає число, яке відповідає ефективному ідентифікатору користувача поточного процесу. Подивіться функцію [posix\_getpwuid()](function.posix-getpwuid.html) для отримання інформації, як перетворити дане число в ім'я користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ID користувача як int

### Приклади

**Приклад #1 Приклад використання **posixgeteuid()****

Даний приклад виводить ID поточного користувача, потім встановлює значення ефективного ідентифікатора користувача, використовуючи функцію [posix\_seteuid()](function.posix-seteuid.html), і показує різницю між дійсним та ефективним ідентифікаторами користувача.

```php
<?php
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_seteuid(10000);
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10000
?>
```

### Дивіться також

-   [posix\_getpwuid()](function.posix-getpwuid.html) - Повертає інформацію про користувача, використовуючи його ID
-   [posix\_getuid()](function.posix-getuid.html) - Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posix\_setuid()](function.posix-setuid.html) - Встановлює UID поточного процесу
-   POSIX керівництво GETEUID(2)