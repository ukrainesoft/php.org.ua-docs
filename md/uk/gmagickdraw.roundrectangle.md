---
navigation:
  - gmagickdraw.rotate.md: '« GmagickDraw::rotate'
  - gmagickdraw.scale.md: 'GmagickDraw::scale »'
  - index.md: PHP Manual
  - class.gmagickdraw.md: GmagickDraw
title: 'GmagickDraw::roundrectangle'
---
# GmagickDraw::roundrectangle

(PECL gmagick >= Unknown)

GmagickDraw::roundrectangle — Малює прямокутник із закругленими кутами.

### Опис

```methodsynopsis
public GmagickDraw::roundrectangle(    float $x1,    float $y1,    float $x2,    float $y2,    float $rx,    float $ry): GmagickDraw
```

Малює прямокутник із закругленими кутами за двома координатами та радіусами кутів x та y, використовуючи поточне обведення, її ширину та налаштування заливки.

### Список параметрів

`x1`

Перша координата x.

`y1`

Перша координата y.

`x2`

Друга координата x.

`y2`

Друга координата y.

`rx`

Радіус кута у горизонтальному напрямку.

`ry`

Радіус кута у вертикальному напрямку.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md)
