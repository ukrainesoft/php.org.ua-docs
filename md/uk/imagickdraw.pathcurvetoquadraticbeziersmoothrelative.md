Малює квадратичну криву Безьє

-   [« ImagickDraw::pathCurveToQuadraticBezierSmoothAbsolute](imagickdraw.pathcurvetoquadraticbeziersmoothabsolute.md)
    
-   [ImagickDraw::pathCurveToRelative »](imagickdraw.pathcurvetorelative.md)
    
-   [PHP Manual](index.md)
    
-   [ImagickDraw](class.imagickdraw.md)
    
-   Малює квадратичну криву Безьє
    

# ImagickDraw::pathCurveToQuadraticBezierSmoothRelative

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToQuadraticBezierSmoothRelative — Малює квадратичну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToQuadraticBezierSmoothRelative(float $x, float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює квадратичну криву Безьє (з використанням відносних координат) від поточної точки до (x, y). Передбачається, що контрольна точка є відображенням контрольної точки попередньої команди щодо поточної точки. (Якщо попередня команда відсутня або не є DrawPathCurveToQuadraticBezierAbsolute, DrawPathCurveToQuadraticBezierRelative, DrawPathCurveToQuadraticBezierSmoothAbsolute або DrawPathCurveToQuadra В кінці команди нова поточна точка стає останньою парою координат (x, y), що використовується в кривій Безьє.

Функцію не можна використовувати для плавного продовження кубічної кривої Безьє. Вона може плавно продовжувати лише квадратичну криву.

### Список параметрів

`x`

Кінцева координата x.

`y`

Кінцева координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::pathCurveToQuadraticBezierSmoothRelative()****

```php
<?php
$draw = new \ImagickDraw();

$draw->setStrokeOpacity(1);
$draw->setStrokeColor("black");
$draw->setFillColor("blue");

$draw->setStrokeWidth(2);
$draw->setFontSize(72);

$draw->pathStart();
$draw->pathMoveToAbsolute(50,250);

// Определение квадратичной кривой Безье с текущей позицией в качестве начальной точки,
// контрольной точкой являются первые два параметра, а конечной - последние два.
$draw->pathCurveToQuadraticBezierAbsolute(
    150,50,
    250,250
);

// Определение квадратичной кривой Безье с текущей позицией в качестве начальной точки,
// контрольная точка зеркально отражается от контрольной точки предыдущей кривой,
// а конечная точка определяется значениями x, y.
$draw->pathCurveToQuadraticBezierSmoothAbsolute(
    450,250
);

// Определение квадратичной кривой Безье с текущей позицией в качестве начальной точки,
// контрольная точка зеркально отражается от контрольной точки предыдущей кривой,
// а конечная точка определяется значениями x, y относительно текущей позиции.
$draw->pathCurveToQuadraticBezierSmoothRelative(
    200,-100
);

$draw->pathFinish();

$imagick = new \Imagick();
$imagick->newImage(700, 500, $backgroundColor);
$imagick->setImageFormat("png");

$imagick->drawImage($draw);

header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```