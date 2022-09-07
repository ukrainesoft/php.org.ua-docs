---
navigation:
  - function.xdiff-file-rabdiff.md: xdifffilerabdiff
  - function.xdiff-string-bdiff.md: xdiffstringbdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiffstringbdiffsize
---
# xdiffstringbdiffsize

(PECL xdiff >= 1.5.0)

xdiffstringbdiffsize — Отримати розмір файлу, створеного після застосування бінарного патчу.

### Опис

```methodsynopsis
xdiff_string_bdiff_size(string $patch): int
```

Повертає розмір файлу, який буде створено після застосування бінарного патчу (`patch`) до оригінального файлу.

### Список параметрів

`patch`

Бінарний патч, створений функціями [xdiffstringbdiff()](function.xdiff-string-bdiff.md) або [xdiffstringrabdiff()](function.xdiff-string-rabdiff.md)

### Значення, що повертаються

Повертає розмір файлу в байтах.

### Приклади

**Приклад #1 Приклад використання **xdiffstringbdiffsize()****

У наступному коді провадиться підрахунок результуючого розміру файлу після застосування бінарного патчу.

```php
<?php
$binary_patch = file_get_contents('file.bdiff');
$length = xdiff_string_bdiff_size($binary_patch);
echo "Результирующий файл будет занимать $length байт";
?>
```

### Дивіться також

-   [xdiffstringbdiff()](function.xdiff-string-bdiff.md) - Створити бінарний патч для двох рядків
-   [xdiffstringrabdiff()](function.xdiff-string-rabdiff.md) - Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
-   [xdiffstringbpatch()](function.xdiff-string-bpatch.md) - Застосування бінарного патча до рядка
