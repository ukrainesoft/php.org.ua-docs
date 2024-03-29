---
navigation:
  - imagickdraw.pathellipticarcabsolute.md: '« ImagickDraw::pathEllipticArcAbsolute'
  - imagickdraw.pathfinish.md: 'ImagickDraw::pathFinish »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pathEllipticArcRelative'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pathEllipticArcRelative

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathEllipticArcRelative — Малює еліптичну дугу

### Опис

```methodsynopsis
public ImagickDraw::pathEllipticArcRelative(    float $rx,    float $ry,    float $x_axis_rotation,    bool $large_arc_flag,    bool $sweep_flag,    float $x,    float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює еліптичну дугу від поточної точки (x, y) з використанням відносних координат. Розмір та орієнтація еліпса визначаються двома радіусами (rx, ry) та параметром xAxisRotation, який вказує, як еліпс загалом обертається щодо поточної системи координат. Центр (cx, cy) еліпса обчислюється автоматично, щоб задовольнити обмеження інших параметрів. largeArcFlag та sweepFlag беруть участь в автоматичних обчисленнях та допомагають визначити, як намальована дуга. Якщо значення `large_arc_flag` одно \*\*`true`\*\*то малюється найбільша з доступних дуг. Якщо значення `sweep_flag` і true, то малюється дуга, що відповідає обертанню за годинниковою стрілкою.

### Список параметрів

`rx`

Радіус x.

`ry`

Радіус y.

`x_axis_rotation`

Обертання осі x.

`large_arc_flag`

Прапор large arc.

`sweep_flag`

Прапор sweep.

`x`

Координата x.

`y`

Координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.
