---
navigation:
  - function.readfile.html: « readfile
  - function.realpath-cache-get.html: realpathcacheget »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: readlink
---
# readlink

(PHP 4, PHP 5, PHP 7, PHP 8)

readlink — Повертає файл, на який вказує символічне посилання

### Опис

```methodsynopsis
readlink(string $path): string|false
```

**readlink()** робить те саме, що і функція C readlink.

### Список параметрів

`path`

Шлях до символічного заслання.

### Значення, що повертаються

Повертає шлях, на який вказує символічне посилання, або **`false`** у разі виникнення помилки.

> **Зауваження**: Функція завершується помилкою, якщо `path` не є символічним посиланням, крім Windows, де буде повернутий нормалізований шлях.

### Приклади

**Приклад #1 Приклад використання функції **readlink()****

```php
<?php

// выведет что-то вроде /boot/vmlinux-2.4.20-xfs
echo readlink('/vmlinuz');

?>
```

### Дивіться також

-   [ісlink()](function.is-link.html) - Визначає, чи є файл символічним посиланням
-   [symlink()](function.symlink.html) - Створює символічне посилання
-   [linkinfo()](function.linkinfo.html) - Повертає інформацію про посилання
