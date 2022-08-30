Закриває зображення та звільняє пам'ять

-   [«psclip](function.ps-clip.html)
    
-   [псclose »](function.ps-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Закриває зображення та звільняє пам'ять
    

# псcloseimage

(PECL ps >= 1.1.0)

псcloseimage — Закриває зображення та звільняє пам'ять

### Опис

```methodsynopsis
ps_close_image(resource $psdoc, int $imageid): void|false
```

Закриває зображення та звільняє його ресурси. Як тільки зображення було закрито, його не можна використовувати.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`imageid`

Ідентифікатор ресурсу зображення, повернутий функцією [псopenimage()](function.ps-open-image.html) або [псopenimagefile()](function.ps-open-image-file.html)

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псopenimage()](function.ps-open-image.html) - Зчитує зображення для подальшого розміщення
-   [псopenimagefile()](function.ps-open-image-file.html) - Відкриває зображення із файлу