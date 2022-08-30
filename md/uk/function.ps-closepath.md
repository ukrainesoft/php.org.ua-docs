Замикає шлях

-   [«psclosepathstroke](function.ps-closepath-stroke.html)
    
-   [псcontinuetext »](function.ps-continue-text.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Замикає шлях
    

# псclosepath

(PECL ps >= 1.1.0)

псclosepath - Замикає шлях

### Опис

```methodsynopsis
ps_closepath(resource $psdoc): bool
```

Поєднує останню точку з першою точкою шляху. Отриманий контур можна використовувати для обведення, заливки, обрізки тощо.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclip()](function.ps-clip.html) - Відображення кліпів по поточному шляху
-   [псclosepathstroke()](function.ps-closepath-stroke.html) - Замикає та обводить контур