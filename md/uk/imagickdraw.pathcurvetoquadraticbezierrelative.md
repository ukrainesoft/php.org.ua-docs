---
navigation:
  - imagickdraw.pathcurvetoquadraticbezierabsolute.md: '« ImagickDraw::pathCurveToQuadraticBezierAbsolute'
  - imagickdraw.pathcurvetoquadraticbeziersmoothabsolute.md: 'ImagickDraw::pathCurveToQuadraticBezierSmoothAbsolute »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pathCurveToQuadraticBezierRelative'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pathCurveToQuadraticBezierRelative

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathCurveToQuadraticBezierRelative — Малює квадратичну криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::pathCurveToQuadraticBezierRelative(    float $x1,    float $y1,    float $x,    float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює квадратичну криву Безьє від поточної точки до (x, y) з (x1, y1) як контрольну точку, використовуючи відносні координати. Наприкінці команди нова поточна точка стає останньою парою координат (x,y), що використовується в кривій Безьє.

### Список параметрів

`x1`

Початкова координата x.

`y1`

Початкова координата y.

`x`

Кінцева координата x.

`y`

Кінцева координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.
