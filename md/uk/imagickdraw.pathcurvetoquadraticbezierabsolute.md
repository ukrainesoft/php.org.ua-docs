---
navigation:
  - imagickdraw.pathcurvetoabsolute.md: '« ImagickDraw::pathCurveToAbsolute'
  - imagickdraw.pathcurvetoquadraticbezierrelative.md: 'ImagickDraw::pathCurveToQuadraticBezierRelative »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pathCurveToQuadraticBezierAbsolute'
---
# ImagickDraw::pathCurveToQuadraticBezierAbsolute

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToQuadraticBezierAbsolute — Малює квадратичну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToQuadraticBezierAbsolute(    float $x1,    float $y1,    float $x,    float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює квадратичну криву Безьє від поточної точки до (x,y) з (x1,y1) як контрольну точку, використовуючи абсолютні координати. Наприкінці команди нова поточна точка стає останньою парою координат (x,y), що використовується в кривій Безьє.

### Список параметрів

`x1`

Координата x контрольної точки.

`y1`

Координата y першої контрольної точки.

`x`

Координата x кінцевої точки.

`y`

Координата y кінцевої точки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::pathCurveToQuadraticBezierAbsolute()****

```php
<?php
function pathCurveToQuadraticBezierAbsolute($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

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

}

?>
```
