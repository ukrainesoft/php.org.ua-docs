Отримати розмір файлу, створеного після застосування бінарного патча

-   [xdifffilerabdiff](function.xdiff-file-rabdiff.html)
    
-   [xdiffstringbdiff »](function.xdiff-string-bdiff.html)
    
-   [PHP Manual](index.html)
    
-   [Функції xdiff](ref.xdiff.html)
    
-   Отримати розмір файлу, створеного після застосування бінарного патча
    

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

Бінарний патч, створений функціями [xdiffstringbdiff()](function.xdiff-string-bdiff.html) або [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html)

### Значення, що повертаються

Повертає розмір файлу в байтах.

### Приклади

**Приклад #1 Приклад використання **xdiffstringbdiffsize()****

У наступному коді провадиться підрахунок результуючого розміру файлу після застосування бінарного патчу.

```php
<?php
$binary_patch = file_get_contents('file.bdiff');
$length = xdiff_string_bdiff_size($binary_patch);
echo "Результирующий файл будет занимать $length байт";
?>
```

### Дивіться також

-   [xdiffstringbdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html) - Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
-   [xdiffstringbpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка