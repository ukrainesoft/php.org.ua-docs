Повертає фактичний ідентифікатор користувача поточного процесу UID

-   [« posixgetsid](function.posix-getsid.html)
    
-   [posixinitgroups »](function.posix-initgroups.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає фактичний ідентифікатор користувача поточного процесу UID
    

# posixgetuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetuid — Повертає фактичний ідентифікатор користувача для поточного процесу UID

### Опис

```methodsynopsis
posix_getuid(): int
```

Повертає число, що відповідає дійсному ID користувача поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ID користувача як int

### Приклади

**Приклад #1 Приклад використання **posixgetuid()****

```php
<?php
echo posix_getuid(); //10000
?>
```

### Дивіться також

-   [posixgetpwuid()](function.posix-getpwuid.html) - Повертає інформацію про користувача, використовуючи його ID
-   POSIX керівництво GETUID(2)