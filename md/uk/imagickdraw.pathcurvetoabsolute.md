Малює кубічну криву Безьє

-   [« ImagickDraw::pathClose](imagickdraw.pathclose.html)
    
-   [ImagickDraw::pathCurveToQuadraticBezierAbsolute »](imagickdraw.pathcurvetoquadraticbezierabsolute.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює кубічну криву Безьє
    

# ImagickDraw::pathCurveToAbsolute

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToAbsolute — Малює кубічну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToAbsolute(    float $x1,    float $y1,    float $x2,    float $y2,    float $x,    float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює кубичну криву Безьє від поточної точки до (x,y), використовуючи (x1,y1) як контрольну точку на початку кривої і (x2,y2) як контрольну точку в кінці кривої з використанням абсолютних координат. Наприкінці команди нова поточна точка стає останньою парою координат (x, y), що використовується в кубічній кривій Безьє.

### Список параметрів

`x1`

Координата першої контрольної точки.

`y1`

Координата y першої контрольної точки.

`x2`

Координата x другої контрольної точки.

`y2`

Координата y другої контрольної точки.

`x`

Координата кінця кривої.

`y`

Координата y кінця кривої.

### Значення, що повертаються

Функція не повертає значення після виконання.