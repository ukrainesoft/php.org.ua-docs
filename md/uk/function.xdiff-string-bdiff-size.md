---
navigation:
  - function.xdiff-file-rabdiff.md: « xdiff\_file\_rabdiff
  - function.xdiff-string-bdiff.md: xdiff\_string\_bdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_bdiff\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_bdiff\_size

(PECL xdiff >= 1.5.0)

xdiff\_string\_bdiff\_size — Отримати розмір файлу, створеного після застосування бінарного патчу.

### Опис

```methodsynopsis
xdiff_string_bdiff_size(string $patch): int
```

Повертає розмір файлу, який буде створено після застосування бінарного патчу (`patch`) до оригінального файлу.

### Список параметрів

`patch`

Бінарний патч, створений функціями [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) або [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md)

### Значення, що повертаються

Повертає розмір файлу в байтах.

### Приклади

**Пример #1 Пример использования**xdiff\_string\_bdiff\_size()\*\*\*\*

У наступному коді провадиться підрахунок результуючого розміру файлу після застосування бінарного патчу.

```php
<?php
$binary_patch = file_get_contents('file.bdiff');
$length = xdiff_string_bdiff_size($binary_patch);
echo "Результирующий файл будет занимать $length байт";
?>
```

### Дивіться також

-   [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) \- Створити бінарний патч для двох рядків
-   [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md) \- Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.md) \- Застосування бінарного патча до рядка
