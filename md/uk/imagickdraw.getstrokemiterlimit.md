---
navigation:
  - imagickdraw.getstrokelinejoin.md: '« ImagickDraw::getStrokeLineJoin'
  - imagickdraw.getstrokeopacity.md: 'ImagickDraw::getStrokeOpacity »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::getStrokeMiterLimit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::getStrokeMiterLimit

(PECL imagick 2, PECL imagick 3)

ImagickDraw::getStrokeMiterLimit — Повертає межу зрізу обведення

### Опис

```methodsynopsis
public ImagickDraw::getStrokeMiterLimit(): int
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Повертає межу зрізу. Коли два відрізки лінії зустрічаються під гострим кутом і для lineJoin задані кутові стики, зріз може виходити далеко за межі товщини лінії, що обводить контур. 'miterLimit' накладає обмеження на відношення довжини зрізу до 'lineWidth'.

### Значення, що повертаються

Повертає ціле число, що описує межу зрізу, або 0, якщо межа зрізу не встановлена.
