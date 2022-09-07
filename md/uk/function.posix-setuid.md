---
navigation:
  - function.posix-setsid.md: « posixsetsid
  - function.posix-strerror.md: posixstrerror »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixsetuid
---
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
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_setuid(10000);
echo posix_getuid()."\n"; //10000
echo posix_geteuid()."\n"; //10000
?>
```

### Дивіться також

-   [posixsetgid()](function.posix-setgid.md) - Встановлює ідентифікатор групи для поточного процесу GID
-   [posixseteuid()](function.posix-seteuid.md) - Встановлює ефективний ідентифікатор користувача для поточного процесу EUID
-   [posixgetuid()](function.posix-getuid.md) - Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posixgeteuid()](function.posix-geteuid.md) - Повертає ефективний ідентифікатор користувача поточного процесу EUID
