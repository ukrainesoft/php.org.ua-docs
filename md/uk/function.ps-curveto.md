---
navigation:
  - function.ps-continue-text.md: « ps\_continue\_text
  - function.ps-delete.md: ps\_delete »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_curveto
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_curveto

(PECL ps >= 1.1.0)

ps\_curveto - Малює криву

### Опис

```methodsynopsis
ps_curveto(    resource $psdoc,    float $x1,    float $y1,    float $x2,    float $y2,    float $x3,    float $y3): bool
```

Додає відрізок кубічної кривої Безьє, описаний трьома заданими контрольними точками, до поточного шляху. points to the current path.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_lineto()](function.ps-lineto.md) \- Малює лінію
