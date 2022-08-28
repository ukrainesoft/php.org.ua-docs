Замикає шлях

-   [« ps\_closepath\_stroke](function.ps-closepath-stroke.html)
    
-   [ps\_continue\_text »](function.ps-continue-text.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_clip()](function.ps-clip.html) - Відображення кліпів по поточному шляху
-   [ps\_closepath\_stroke()](function.ps-closepath-stroke.html) - Замикає та обводить контур