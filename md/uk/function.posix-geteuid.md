---
navigation:
  - function.posix-getegid.md: « posixgetegid
  - function.posix-getgid.md: posixgetgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgeteuid
---
# posixgeteuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgeteuid — Повертає ефективний ідентифікатор користувача поточного процесу EUID

### Опис

```methodsynopsis
posix_geteuid(): int
```

Повертає число, яке відповідає ефективному ідентифікатору користувача поточного процесу. Подивіться функцію [posixgetpwuid()](function.posix-getpwuid.md) для отримання інформації, як перетворити дане число в ім'я користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ID користувача як int

### Приклади

**Приклад #1 Приклад використання **posixgeteuid()****

Даний приклад виводить ID поточного користувача, потім встановлює значення ефективного ідентифікатора користувача, використовуючи функцію [posixseteuid()](function.posix-seteuid.md), і показує різницю між дійсним та ефективним ідентифікаторами користувача.

```php
<?php
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_seteuid(10000);
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10000
?>
```

### Дивіться також

-   [posixgetpwuid()](function.posix-getpwuid.md) - Повертає інформацію про користувача, використовуючи його ID
-   [posixgetuid()](function.posix-getuid.md) - Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posixsetuid()](function.posix-setuid.md) - Встановлює UID поточного процесу
-   POSIX керівництво GETEUID(2)
