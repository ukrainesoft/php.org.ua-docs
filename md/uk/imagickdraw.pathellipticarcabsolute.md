Малює еліптичну дугу

-   [« ImagickDraw::pathCurveToSmoothRelative](imagickdraw.pathcurvetosmoothrelative.html)
    
-   [ImagickDraw::pathEllipticArcRelative »](imagickdraw.pathellipticarcrelative.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює еліптичну дугу
    

# ImagickDraw::pathEllipticArcAbsolute

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pathEllipticArcAbsolute — Малює еліптичну дугу

### Опис

```methodsynopsis
public ImagickDraw::pathEllipticArcAbsolute(    float $rx,    float $ry,    float $x_axis_rotation,    bool $large_arc_flag,    bool $sweep_flag,    float $x,    float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює еліптичну дугу від поточної точки (x, y) з використанням абсолютних координат. Розмір та орієнтація еліпса визначаються двома радіусами (rx, ry) та параметром xAxisRotation, який вказує, як еліпс загалом обертається щодо поточної системи координат. Центр (cx, cy) еліпса обчислюється автоматично, щоб задовольнити обмеження інших параметрів. largeArcFlag та sweepFlag беруть участь в автоматичних обчисленнях та допомагають визначити, як намальована дуга. Якщо значення `large_arc_flag` одно \*\*`true`\*\*то малюється найбільша з доступних дуг. Якщо значення `sweep_flag` і true, то малюється дуга, що відповідає обертанню за годинниковою стрілкою.

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