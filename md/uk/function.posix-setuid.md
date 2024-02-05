---
navigation:
  - function.posix-setsid.md: « posix\_setsid
  - function.posix-strerror.md: posix\_strerror »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_setuid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_setuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_setuid — Встановлює UID поточного процесу

### Опис

```methodsynopsis
posix_setuid(int $user_id): bool
```

Встановлює фактичний ідентифікатор користувача цього процесу. Це привілейований процес і вимагає відповідних прав (зазвичай прав суперкористувача root) у системі для можливості виконати цю функцію.

### Список параметрів

`user_id`

Ідентифікатор користувача.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_setuid()\*\*\*\*

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

-   [posix\_setgid()](function.posix-setgid.md) \- Встановлює ідентифікатор групи для поточного процесу GID
-   [posix\_seteuid()](function.posix-seteuid.md) \- Встановлює ефективний ідентифікатор користувача для поточного процесу EUID
-   [posix\_getuid()](function.posix-getuid.md) \- Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posix\_geteuid()](function.posix-geteuid.md) \- Повертає ефективний ідентифікатор користувача поточного процесу EUID
