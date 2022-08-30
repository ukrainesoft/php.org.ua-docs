Встановлює UID поточного процесу

-   [« posixsetsid](function.posix-setsid.html)
    
-   [posixstrerror »](function.posix-strerror.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Встановлює UID поточного процесу
    

# posixsetuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixsetuid — Встановлює UID поточного процесу

### Опис

```methodsynopsis
posix_setuid(int $user_id): bool
```

Встановлює фактичний ідентифікатор користувача цього процесу. Це привілейований процес і потребує відповідних прав (зазвичай прав суперкористувача root) у системі для можливості виконати цю функцію.

### Список параметрів

`user_id`

Ідентифікатор користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixsetuid()****

Цей код виводить поточний ідентифікатор користувача, а потім змінює його.

```php
<?php
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_setuid(10000);
echo posix_getuid()."\n"; //10000
echo posix_geteuid()."\n"; //10000
?>
```

### Дивіться також

-   [posixsetgid()](function.posix-setgid.html) - Встановлює ідентифікатор групи для поточного процесу GID
-   [posixseteuid()](function.posix-seteuid.html) - Встановлює ефективний ідентифікатор користувача для поточного процесу EUID
-   [posixgetuid()](function.posix-getuid.html) - Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posixgeteuid()](function.posix-geteuid.html) - Повертає ефективний ідентифікатор користувача поточного процесу EUID