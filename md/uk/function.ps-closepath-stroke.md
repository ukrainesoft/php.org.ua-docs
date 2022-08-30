Замикає та обводить контур

-   [«psclose](function.ps-close.html)
    
-   [псclosepath »](function.ps-closepath.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Замикає та обводить контур
    

# псclosepathstroke

(PECL ps >= 1.1.0)

псclosepathstroke — Замикає та обводить контур

### Опис

```methodsynopsis
ps_closepath_stroke(resource $psdoc): bool
```

З'єднує останню точку з першою точкою шляху і малює замкнуту лінію, що вийшла.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclosepath()](function.ps-closepath.html) - Замикає шлях