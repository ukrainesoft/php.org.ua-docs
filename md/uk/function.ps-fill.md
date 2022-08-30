Заповнює поточний шлях

-   [«psfillstroke](function.ps-fill-stroke.html)
    
-   [псfindfont »](function.ps-findfont.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Заповнює поточний шлях
    

# псfill

(PECL ps >= 1.1.0)

псfill — Заповнює поточний шлях

### Опис

```methodsynopsis
ps_fill(resource $psdoc): bool
```

Заповнює шлях, створений за допомогою раніше викликаних функцій малювання, таких як [псlineto()](function.ps-lineto.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псfillstroke()](function.ps-fill-stroke.html) - Заповнює та обводить поточний шлях
-   [псstroke()](function.ps-stroke.html) - Малює поточний шлях