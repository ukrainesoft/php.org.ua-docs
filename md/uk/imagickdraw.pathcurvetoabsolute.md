---
navigation:
  - imagickdraw.pathclose.md: '« ImagickDraw::pathClose'
  - imagickdraw.pathcurvetoquadraticbezierabsolute.md: 'ImagickDraw::pathCurveToQuadraticBezierAbsolute »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pathCurveToAbsolute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pathCurveToAbsolute

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToAbsolute — Малює кубічну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToAbsolute(    float $x1,    float $y1,    float $x2,    float $y2,    float $x,    float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

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
