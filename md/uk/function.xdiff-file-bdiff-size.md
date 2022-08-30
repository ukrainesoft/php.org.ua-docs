Отримати розмір файлу після застосування бінарного патчу

-   [« Функції xdiff](ref.xdiff.html)
    
-   [xdifffilebdiff »](function.xdiff-file-bdiff.html)
    
-   [PHP Manual](index.html)
    
-   [Функції xdiff](ref.xdiff.html)
    
-   Отримати розмір файлу після застосування бінарного патчу
    

# xdifffilebdiffsize

(PECL xdiff >= 1.5.0)

xdifffilebdiffsize — Отримати розмір файлу після застосування бінарного патчу

### Опис

```methodsynopsis
xdiff_file_bdiff_size(string $file): int
```

Повертає розмір файлу, який буде створено після застосування бінарного патчу з файлу `file`

### Список параметрів

`file`

Шлях до бінарного патчу, створеного функціями [xdiffstringbdiff()](function.xdiff-string-bdiff.html) або [xdiffstringrabdiff()](function.xdiff-string-rabdiff.html)

### Значення, що повертаються

Повертає розмір файлу, який буде створено.

### Приклади

**Приклад #1 Приклад використання **xdifffilebdiffsize()****

Наступний код отримує розмір файлу, створеного після застосування патча.

```php
<?php
$length = xdiff_string_bdiff_size('file.bdiff');
echo "Размер результирующего файла будет $length байт";
?>
```

### Дивіться також

-   [xdifffilebdiff()](function.xdiff-file-bdiff.html) - Створити бінарний патч порівнюючи два файли
-   [xdifffilerabdiff()](function.xdiff-file-rabdiff.html) - Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting
-   [xdifffilebpatch()](function.xdiff-file-bpatch.html) - Застосувати бінарний патч до файлу