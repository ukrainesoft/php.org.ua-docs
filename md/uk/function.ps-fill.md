Заповнює поточний шлях

-   [« ps\_fill\_stroke](function.ps-fill-stroke.html)
    
-   [ps\_findfont »](function.ps-findfont.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Заповнює поточний шлях
    

# псfill

(PECL ps >= 1.1.0)

псfill — Заповнює поточний шлях

### Опис

```methodsynopsis
ps_fill(resource $psdoc): bool
```

Заповнює шлях, створений за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_fill\_stroke()](function.ps-fill-stroke.html) - Заповнює та обводить поточний шлях
-   [ps\_stroke()](function.ps-stroke.html) - Малює поточний шлях