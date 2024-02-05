---
navigation:
  - function.readfile.md: « readfile
  - function.realpath-cache-get.md: realpath\_cache\_get »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: readlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає шлях, на який вказує символічне посилання, або \*\*`false`\*\*в случае возникновения ошибки.

> **Зауваження**: Функція завершується помилкою, якщо `path` не є символічним посиланням, крім Windows, де буде повернутий нормалізований шлях.

### Приклади

**Пример #1 Пример использования функции**readlink()\*\*\*\*

```php
<?php

// выведет что-то вроде /boot/vmlinux-2.4.20-xfs
echo readlink('/vmlinuz');

?>
```

### Дивіться також

-   [is\_link()](function.is-link.md) \- Визначає, чи є файл символічним посиланням
-   [symlink()](function.symlink.md) \- Створює символічне посилання
-   [linkinfo()](function.linkinfo.md) \- Повертає інформацію про посилання
