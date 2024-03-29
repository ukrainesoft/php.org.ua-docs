---
navigation:
  - imagickdraw.pathcurvetoquadraticbeziersmoothrelative.md: '« ImagickDraw::pathCurveToQuadraticBezierSmoothRelative'
  - imagickdraw.pathcurvetosmoothabsolute.md: 'ImagickDraw::pathCurveToSmoothAbsolute »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pathCurveToRelative'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pathCurveToRelative

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToRelative — Малює кубічну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToRelative(    float $x1,    float $y1,    float $x2,    float $y2,    float $x,    float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює кубичну криву Безьє від поточної точки до (x,y), використовуючи (x1,y1) як контрольну точку на початку кривої і (x2,y2) як контрольну точку в кінці кривої з використанням відносних координат. Наприкінці команди нова поточна точка стає останньою парою координат (x,y), що використовується в кубічній кривій Безьє.

### Список параметрів

`x1`

Координата x початкової контрольної точки.

`y1`

Координата y початкової контрольної точки.

`x2`

Координата x кінцевої контрольної точки.

`y2`

Координата y кінцевої контрольної точки.

`x`

Кінцева координата x.

`y`

Кінцева координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.
