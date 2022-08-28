Заповнює та обводить поточний шлях

-   [« ps\_end\_template](function.ps-end-template.html)
    
-   [ps\_fill »](function.ps-fill.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Заповнює та обводить поточний шлях
    

# псfillstroke

(PECL ps >= 1.1.0)

псfillstroke — Заповнює та обводить поточний шлях

### Опис

```methodsynopsis
ps_fill_stroke(resource $psdoc): bool
```

Заповнює та обводить шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_fill()](function.ps-fill.html) - Заповнює поточний шлях
-   [ps\_stroke()](function.ps-stroke.html) - Малює поточний шлях