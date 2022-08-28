Малює поточний шлях

-   [« ps\_stringwidth](function.ps-stringwidth.html)
    
-   [ps\_symbol\_name »](function.ps-symbol-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Малює поточний шлях
    

# псstroke

(PECL ps >= 1.1.0)

псstroke — Малює поточний шлях

### Опис

```methodsynopsis
ps_stroke(resource $psdoc): bool
```

Малює шлях, побудований за допомогою раніше викликаних функцій малювання, таких як [ps\_lineto()](function.ps-lineto.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_closepath\_stroke()](function.ps-closepath-stroke.html) - Замикає та обводить контур
-   [ps\_fill()](function.ps-fill.html) - Заповнює поточний шлях
-   [ps\_fill\_stroke()](function.ps-fill-stroke.html) - Заповнює та обводить поточний шлях