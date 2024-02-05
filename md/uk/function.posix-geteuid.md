---
navigation:
  - function.posix-getegid.md: « posix\_getegid
  - function.posix-getgid.md: posix\_getgid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_geteuid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_geteuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_geteuid — Повертає ефективний ідентифікатор користувача поточного процесу EUID

### Опис

```methodsynopsis
posix_geteuid(): int
```

Повертає число, яке відповідає ефективному ідентифікатору користувача поточного процесу. Подивіться функцію [posix\_getpwuid()](function.posix-getpwuid.md) для отримання інформації, як перетворити дане число в ім'я користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ID користувача як int

### Приклади

**Пример #1 Пример использования**posix\_geteuid()\*\*\*\*

Даний приклад виводить ID поточного користувача, потім встановлює значення ефективного ідентифікатора користувача, використовуючи функцію [posix\_seteuid()](function.posix-seteuid.md), і показує різницю між дійсним та ефективним ідентифікаторами користувача.

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

-   [posix\_getpwuid()](function.posix-getpwuid.md) \- Повертає інформацію про користувача, використовуючи його ID
-   [posix\_getuid()](function.posix-getuid.md) \- Повертає фактичний ідентифікатор користувача поточного процесу UID
-   [posix\_setuid()](function.posix-setuid.md) \- Встановлює UID поточного процесу
-   POSIX керівництво GETEUID(2)
