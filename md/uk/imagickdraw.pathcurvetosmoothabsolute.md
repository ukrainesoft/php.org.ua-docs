Малює кубічну криву Безьє

-   [« ImagickDraw::pathCurveToRelative](imagickdraw.pathcurvetorelative.html)
    
-   [ImagickDraw::pathCurveToSmoothRelative »](imagickdraw.pathcurvetosmoothrelative.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює кубічну криву Безьє
    

# ImagickDraw::pathCurveToSmoothAbsolute

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToSmoothAbsolute — Малює кубічну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToSmoothAbsolute(    float $x2,    float $y2,    float $x,    float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює кубичну криву Безьє від поточної точки до (x, y) з використанням абсолютних координат. Передбачається, що перша контрольна точка є відображенням другої контрольної точки попередньої команди щодо поточної точки. (Якщо попередня команда відсутня або не є DrawPathCurveToAbsolute, DrawPathCurveToRelative, DrawPathCurveToSmoothAbsolute або DrawPathCurveToSmoothRelative, то передбачається, що перша контрольна точка збігається з . (x2, y2) – друга контрольна точка (тобто контрольна точка в кінці кривої). В кінці команди нова поточна точка стає останньою парою координат (x, y), що використовується в кривій Безьє.

### Список параметрів

`x2`

Координата x другої контрольної точки.

`y2`

Координата y другої контрольної точки.

`x`

Координата x кінцевої точки.

`y`

Координата y кінцевої точки.

### Значення, що повертаються

Функція не повертає значення після виконання.