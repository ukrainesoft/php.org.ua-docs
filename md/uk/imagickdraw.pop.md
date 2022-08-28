Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw

-   [« ImagickDraw::polyline](imagickdraw.polyline.html)
    
-   [ImagickDraw::popClipPath »](imagickdraw.popclippath.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw
    

# ImagickDraw::pop

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pop — Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw

### Опис

```methodsynopsis
public ImagickDraw::pop(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Знищує поточний об'єкт ImagickDraw у стеку та повертається до раніше доданого об'єкту ImagickDraw. Може бути кілька зображень ImagickDraw. Спроба витягти більше зображень ImagickDraw, ніж було додано, призведе до виникнення помилки, правильним використанням є вилучення лише зображень ImagickDraw, які були додані в стек.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.