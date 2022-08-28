Отримати розмір файлу, створеного після застосування бінарного патча

-   [« xdiff\_file\_rabdiff](function.xdiff-file-rabdiff.html)
    
-   [xdiff\_string\_bdiff »](function.xdiff-string-bdiff.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
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

Бінарний патч, створений функціями [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.html) або [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.html)

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

-   [xdiff\_string\_bdiff()](function.xdiff-string-bdiff.html) - Створити бінарний патч для двох рядків
-   [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.html) - Порівняти два рядки та створити бінарний патч використовуючи поліномінальний алгоритм Rabin fingerprint
-   [xdiff\_string\_bpatch()](function.xdiff-string-bpatch.html) - Застосування бінарного патча до рядка