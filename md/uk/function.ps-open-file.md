Відкриває файл для виводу

-   [« ps\_new](function.ps-new.html)
    
-   [ps\_open\_image\_file »](function.ps-open-image-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Відкриває файл для виводу
    

# псopenfile

(PECL ps >= 1.1.0)

псopenfile — Відкриває файл для виводу

### Опис

```methodsynopsis
ps_open_file(resource $psdoc, string $filename = ?): bool
```

Створює новий файл на диску і записує документ PostScript. Файл буде закрито під час виклику [ps\_close()](function.ps-close.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`filename`

Назва файлу postscript. Якщо `filename` не передано, документ буде створено в пам'яті і весь висновок йтиме прямо до браузера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_close()](function.ps-close.html) - Закриває документ PostScript