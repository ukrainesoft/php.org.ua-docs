---
navigation:
  - imagickdraw.clone.md: '« ImagickDraw::clone'
  - imagickdraw.comment.md: 'ImagickDraw::comment »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::color'
---
# ImagickDraw::color

(PECL imagick 2, PECL imagick 3)

ImagickDraw::color — Малює колір на зображенні

### Опис

```methodsynopsis
public ImagickDraw::color(float $x, float $y, int $paintMethod): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює колір на зображенні, використовуючи поточний колір заливки, починаючи з вказаної позиції та використовуючи вказаний метод малювання.

### Список параметрів

`x`

Координата X малюнка

`y`

Координата Y малюнка

`paintMethod`

Одна з констант [PAINT](imagick.constants.html#imagick.constants.paint) `imagick::PAINT_*`

### Значення, що повертаються

Функція не повертає значення після виконання.
