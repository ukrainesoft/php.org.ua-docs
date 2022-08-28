Встановлює значення сірого

-   [« ps\_setfont](function.ps-setfont.html)
    
-   [ps\_setlinecap »](function.ps-setlinecap.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює значення сірого
    

# псsetgray

(PECL ps >= 1.1.0)

псsetgray - Встановлює значення сірого

### Опис

```methodsynopsis
ps_setgray(resource $psdoc, float $gray): bool
```

Встановлює значення сірого всіх наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`gray`

Значення повинне бути від 0 (білий) до 1 (чорний).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_setcolor()](function.ps-setcolor.html) - Встановлює поточний колір