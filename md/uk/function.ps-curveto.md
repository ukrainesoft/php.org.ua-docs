---
navigation:
  - function.ps-continue-text.md: «pscontinuetext
  - function.ps-delete.md: псdelete »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псcurveto
---
# псcurveto

(PECL ps >= 1.1.0)

псcurveto - Малює криву

### Опис

```methodsynopsis
ps_curveto(    resource $psdoc,    float $x1,    float $y1,    float $x2,    float $y2,    float $x3,    float $y3): bool
```

Додає відрізок кубічної кривої Безьє, описаний трьома заданими контрольними точками, до поточного шляху. points to the current path.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`x1`

Координата X першої контрольної точки.

`y1`

Координата Y першої контрольної точки.

`x2`

Координата X другої контрольної точки.

`y2`

Координата Y другої контрольної точки.

`x3`

Координата X третьої контрольної точки.

`y3`

Координата Y третьої контрольної точки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псlineto()](function.ps-lineto.md) - Малює лінію
