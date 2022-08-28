Закриває документ PostScript

-   [« ps\_close\_image](function.ps-close-image.html)
    
-   [ps\_closepath\_stroke »](function.ps-closepath-stroke.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Закриває документ PostScript
    

# псclose

(PECL ps >= 1.1.0)

псclose — Закриває документ PostScript

### Опис

```methodsynopsis
ps_close(resource $psdoc): bool
```

Закриває документ PostScript.

Функція записує кількість сторінок у документі PostScript. Вона також записує ієрархію закладок . **псclose()** не звільняє ресурси, як [ps\_delete()](function.ps-delete.html)

Функція також викликається функцією [ps\_delete()](function.ps-delete.html)якщо вона не була викликана раніше.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_open\_file()](function.ps-open-file.html) - Відкриває файл для виводу
-   [ps\_delete()](function.ps-delete.html) - Видаляє всі ресурси документа PostScript